아키텍쳐에 따라 바꿔서 쓰시면 됩니다.
```
from pwn import *

# libc = ELF("/lib/x86_64-linux-gnu/libc.so.6")
# libc = ELF("/lib/i386-linux-gnu/libc.so.6")

p = process("./file_name")
e = ELF("./file_name")


def slog(name, addr): return success(': '.join([name, hex(addr)]))

p.interactive()
```