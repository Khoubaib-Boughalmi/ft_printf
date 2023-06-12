# ft_printf

## Description
The ft_printf project is a recoding of the standard C library function `printf`. The function `ft_printf` is designed to mimic the behavior of `printf` and provides a formatted output functionality. This project aims to enhance understanding of the inner workings of `printf` and improve programming skills.

## Function Prototype
```c
int ft_printf(const char *format, ...);
```

## Buffer Management
Unlike the original `printf` function, the buffer management is not implemented in `ft_printf`. The function directly writes the formatted output to the standard output.

## Supported Conversions
`ft_printf` manages the following conversion specifiers:

- `%s` and `%S`: Format and print strings (ASCII and wide characters).
- `%p`: Print memory addresses.
- `%d`, `%D`, `%i`: Format and print signed decimal integers.
- `%o`, `%O`: Format and print unsigned octal integers.
- `%u`, `%U`: Format and print unsigned decimal integers.
- `%x`, `%X`: Format and print unsigned hexadecimal integers.
- `%c`, `%C`: Format and print characters (ASCII and wide characters).

## Special Characters
- `%%`: Prints a single percent character.

## Flags
`ft_printf` supports the following flags:

- `#`: Used for alternative output formatting, depending on the conversion specifier.
- `0`: The value will be padded with zeros instead of spaces.
- `-`: The value will be left-aligned.
- `+`: Forces the sign (`+` or `-`) to be printed for signed conversions.
- `space`: Prints a space before a positive number.

## Minimum Field Width
The minimum field width specifies the minimum number of characters to be printed. If the value to be printed is shorter than the minimum width, it will be padded with spaces (or zeros if the `0` flag is present).

## Precision
The precision specifies the maximum number of characters to be printed. For strings, it determines the maximum length to be printed. For numeric conversions, it sets the number of digits to be printed.

## Length Modifiers
`ft_printf` supports the following length modifiers:

- `hh`: Treats the argument as a signed or unsigned char.
- `h`: Treats the argument as a signed or unsigned short.
- `l`: Treats the argument as a signed or unsigned long.
- `ll`: Treats the argument as a signed or unsigned long long.
- `j`: Treats the argument as an intmax_t or uintmax_t.
- `z`: Treats the argument as a size_t.

## Example Usage
```c
#include "ft_printf.h"

int main(void) {
    ft_printf("Hello, %s! The answer is %d.\n", "world", 42);
    return 0;
}
```

## Compilation
Compile the `ft_printf` library by running the following command:

```bash
gcc -Wall -Wextra -Werror -Iincludes -c srcs/*.c
```

Link the object files to your program:

```bash
gcc -o myprogram main.o ft_printf.o
```

## Resources
- [C - printf format options](https://www.tutorialspoint.com/c_standard_library/c_function_printf.htm)
- [GNU C Library - Formatting Printf](https://www.gnu.org/software/libc/manual/html_node/Formatting-Printf.html)
- [man printf](https://linux.die.net/man/3/printf)
