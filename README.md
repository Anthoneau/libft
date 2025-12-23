# libft

This repository contains my personal **libft**, originally started during the 42 core curriculum and progressively extended and refined throughout my C projects.

More than a school project, this libft has become a **utility library** I reuse consistently to speed up development, reduce boilerplate, and keep my codebase clean and readable.

---

## Build & Usage

### Compilation

```bash
make
```

This will generate the static library:

```
libft.a
```

### Usage in a project

1. Include the header:
```c
#include "libft.h"
```

2. Compile your project with `libft.a`:
```bash
cc your_files.c libft.a
```

---

## Project Philosophy

- Functions are grouped by **purpose**, not by school constraints.
- Frequently re-written helpers were promoted into reusable functions.
- The library grows with real project needs, not artificially.
- Some classic projects from the 42 curriculum (like `get_next_line` and `ft_printf`) are integrated because they are **used constantly**.

This libft is meant to be **practical**, **coherent**, and **production-oriented**.

---

## Project Structure

```text
include/
└── libft.h        # Main header

src/
├── ft_is/         # Character & string checks
├── ft_mem/        # Memory manipulation
├── ft_put/        # Output utilities (fd-based)
├── ft_str/        # String manipulation
├── ft_to/         # Conversions & transformations
├── ft_lst/        # Linked list utilities
├── ft_printf/     # Custom printf implementation
├── gnl/           # get_next_line
└── ft_add/        # Additional / bonus helpers
```

Each directory focuses on a **single responsibility**, making the library easy to navigate and extend.

---

## Module Overview

### `ft_is/` – Checks & Validation
Functions used to validate characters or strings.

Includes helpers such as:
- Alphanumeric / digit / ASCII checks
- Numeric string validation (`ft_isnum`)
- Whitespace-only string validation (`ft_isspace`)

Useful for input validation and parsing.

---

### `ft_mem/` – Memory Utilities
Low-level memory manipulation helpers used throughout the library.

They provide safe and consistent memory handling across all projects.

---

### `ft_put/` – Output Helpers
Simple wrappers to write characters, strings, and numbers to a file descriptor.

Mostly used for logging, debugging, or CLI output.

---

### `ft_str/` – String Manipulation
All string-related utilities live here.

This module allows you to:
- Create, split, trim, or join strings
- Safely copy and concatenate
- Iterate or map over characters

One of the most frequently used parts of the library.

---

### `ft_to/` – Conversions & Transformations
Functions that convert data from one form to another.

Includes:
- String to integer conversions
- Integer to string conversion
- Case transformations
- Base-aware conversions (`ft_atoi_base`)

`itoa` is kept here as a conversion utility rather than a string manipulation function.

---

### `ft_lst/` – Linked List Utilities
A complete linked list API:
- Creation and deletion
- Iteration and mapping
- Size and access helpers

Used whenever dynamic collections are required.

---

### `ft_printf/` – Custom printf
A full reimplementation of the standard `printf` function, developed as part of the 42 core curriculum and fully integrated into this library.

This implementation supports the most commonly used format specifiers:
- `%c` for characters
- `%s` for strings
- `%d` / `%i` for signed integers
- `%u` for unsigned integers
- `%x` / `%X` for hexadecimal output
- `%p` for pointer addresses
- `%%` to print a literal percent sign

The project relies on variadic arguments and custom display functions, making it a solid foundation for formatted output handling while remaining lightweight and fully controlled.

---

### `gnl/` – get_next_line
`get_next_line` is included directly in libft as a core utility.

This project provides a reliable way to read from a file descriptor **line by line**, handling buffering, memory allocation, and edge cases such as partial reads or end-of-file conditions.

It is especially useful in projects involving file manipulation or input stream processing, where controlled and incremental reading is required.

---

### `ft_add/` – Additional Helpers (Bonus)
This directory contains utility functions that are not part of the original libft subject but proved useful across multiple projects.

#### `free_array`
Safely frees a `char **` array and all its contents.

#### `ft_free`
Frees a pointer only if it is not `NULL`, helping keep code clean and norm-compliant (42 norm).

#### `ft_swap`
Swaps the values of two integers.

These helpers reduce repetition and improve code readability across projects.

---

## Conclusion

This libft is a **living library**, shaped by real usage and practical needs rather than academic constraints.

It reflects:
- A focus on reuse and clarity
- Practical experience from multiple C projects
- A solid foundation for larger and more complex codebases

---

## Author

**Anthony Goldberg** ***agoldber***

42 student – core curriculum completed
