# libft

A custom C library developed as part of the 42 Common Core curriculum.

`libft` reimplements a collection of standard C library functions and provides additional utilities for string manipulation, memory management, character handling, and linked lists.

The goal of this project is to strengthen my understanding of C, pointers, memory allocation, and modular code organization.

## Contents

- [Features](#features)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Features

### Character Handling

- `ft_isalpha`
- `ft_isdigit`
- `ft_isalnum`
- `ft_isascii`
- `ft_isprint`
- `ft_tolower`
- `ft_toupper`

### Memory Management

- `ft_memset`
- `ft_bzero`
- `ft_memcpy`
- `ft_memmove`
- `ft_memchr`
- `ft_memcmp`
- `ft_calloc`

### String Manipulation

- `ft_strlen`
- `ft_strlcpy`
- `ft_strlcat`
- `ft_strchr`
- `ft_strrchr`
- `ft_strncmp`
- `ft_strnstr`
- `ft_strdup`
- `ft_substr`
- `ft_strjoin`
- `ft_strtrim`
- `ft_split`
- `ft_itoa`
- `ft_strmapi`
- `ft_striteri`
- `ft_atoi`

### Output Functions

- `ft_putchar_fd`
- `ft_putstr_fd`
- `ft_putendl_fd`
- `ft_putnbr_fd`

### Linked Lists

The library also includes a singly linked list implementation using the `t_list` structure.

- `ft_lstnew`
- `ft_lstadd_front`
- `ft_lstadd_back`
- `ft_lstsize`
- `ft_lstlast`
- `ft_lstdelone`
- `ft_lstclear`
- `ft_lstiter`
- `ft_lstmap`

## Requirements

- GCC or another compatible C compiler
- GNU Make
- A Unix-like environment

The project is compiled with the following warning flags:

`-Wall -Wextra -Werror`

## Getting Started

Clone the repository:

```bash
git clone git@github.com:ItSus14/libft.git
cd libft
```

Build the library:

```bash
make
```

This generates the static library `libft.a`.

To remove object files:

```bash
make clean
```

To remove object files and the compiled library:

```bash
make fclean
```

To rebuild the library:

```bash
make re
```

The project also provides a `bonus` target for compiling the linked-list functions.

## Usage

Include the library header in your C source file:

```c
#include "libft.h"

int main(void)
{
    char *text;

    text = ft_strdup("Hello, world!");
    if (!text)
        return (1);

    ft_putendl_fd(text, 1);
    free(text);
    return (0);
}
```

Compile your program and link it against the library:

```bash
gcc -Wall -Wextra -Werror main.c -L. -lft -o program
```

Run the executable:

```bash
./program
```

## Project Structure

```text
libft/
├── libft.h
├── Makefile
├── ft_*.c
└── README.md
```

## Learning Objectives

- Practice implementing C library functions.
- Improve pointer handling and memory management.
- Work with strings, buffers, and linked lists.
- Organize and compile a multi-file C project.
- Use Git and GitHub to maintain a version-controlled codebase.

---

**Part of my 42 Common Core journey.**
