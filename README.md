아키텍쳐에 따라 바꿔서 쓰시면 됩니다.
```
from pwn import *
context.arch = 'x64'

p = process("./file_name")
e = ELF("./file_name")
libc = ELF("libc.so.6')

def slog(name, addr): return success(': '.join([name, hex(addr)]))

p.interactive()
```
