The foci of this repository are the [logger.c](https://github.com/Valkryst/C_Logging/blob/main/src/logger.c)
and [logger.h](https://github.com/Valkryst/C_Logging/blob/main/src/logger.h)
files. They define the `printError` function which allows you to print detailed
and descriptive error messages to aid in development and debugging.

## Compiling

Add `logger.c` and `logger.h` to your project, update your build script, and
compile as you normally would.

See the provided [Makefile](https://github.com/Valkryst/C_Mutex/blob/main/Makefile)
as a reference.

## Usage

See [C_Mutex](https://github.com/Valkryst/C_Mutex/blob/main/src/mutex.c) and
[C_PThread](https://github.com/Valkryst/C_PThread) as references.

Parameters:

1. If you know that an error has occured and that [errno](https://www.cplusplus.com/reference/cerrno/errno/) has been set, then set the first parameter to `errno`. Else set it to `0`.
2. This should be set to [__FILE__](https://www.cprogramming.com/reference/preprocessor/__FILE__.html), but it also accepts `NULL`.
3. This should be set to [__PRETTY_FUNCTION__](https://gcc.gnu.org/onlinedocs/gcc/Function-Names.html), but it also accepts `NULL`.
4. This should contain a descriptive error message, specific to your program, and should contain information helpful in debugging the related error. This also accepts `NULL`.

Example:

```c
printError(errno, __FILE__, __PRETTY_FUNCTION__, "Some error message.");
```
