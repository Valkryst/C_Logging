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

See [C_Mutex](https://github.com/Valkryst/C_Mutex/blob/main/src/mutex.c) as a
reference.

When you know that an error will set `errno`:

```c
printError(errno, __FILE__, __PRETTY_FUNCTION__, "Some error message.");
```

When you know that an error will not set `errno`:

```c
printError(errno, __FILE__, __PRETTY_FUNCTION__, "Some error message.");
```