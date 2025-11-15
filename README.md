# trypwnme-hack-pwntools-skelleton

from pwn import *

p = process("./rtl")
e = ELF("./rtl")
libc = ELF("./libc.so.6")

def slog(name, addr): return success(': '.join([name, hex(addr)]))

p.interactive()
