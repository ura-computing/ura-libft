# ura-libft

42's libft (`_libft.pdf`, version 17) written in [ura](https://github.com/ura-computing/ura-lang). The functions live in one `mod ft`, so `ft_strlen` is `ft::strlen`.

## Use it

```ura
// ura.conf
@dependency "ura-libft" "0.0.1" "https://github.com/ura-computing/ura-libft"
```

```ura
use "@/libft"

fn main() i32:
    io::out($"{ft::strlen("abc")}\n")      // 3
    ft::putnbr_fd(-42, 1)                   // -42
    return 0
```

## Test it

```bash
ura install
ura test
```

`tests/main.ura` calls every function and prints the results.

## Files

They follow the subject: one file per part, functions in the subject's order.

| file | part | functions |
|---|---|---|
| `ft/libc.ura` | Part 1 - Libc functions | isalpha isdigit isalnum isascii isprint strlen memset bzero memcpy memmove strlcpy strlcat toupper tolower strchr strrchr strncmp memchr memcmp strnstr atoi calloc strdup |
| `ft/additional.ura` | Part 2 - Additional functions | substr strjoin strtrim split itoa putchar_fd putstr_fd putendl_fd putnbr_fd |
| `libft.ura` | | `mod ft:` uses both files |

The prototypes are the subject's, in ura types: `char[]` for `char *` and `void *`, `u64` for `size_t`, `u32` for `unsigned int`, `i32` for `int`.

## Not yet

strmapi, striteri and the bonus (lists) take function arguments, which ura doesn't have yet. They come when function values do.
