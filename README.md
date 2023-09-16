# linux-rootkit
 Kernel <-> Userland
 Ring0

Hooks the LKM and bypasses ASLR, DEP, NX bit, Canaries, etc mostly with gadgets and ROP chains but other tricks are involved. We also move glibc to the side as well, he is not needed.

## About

This attacks multiple architectures with vmalloc() -> kmem() and kmem() -> (ask me more)

### Installation

```bash
# Commands
$ git clone https://github.com/awknode/linux-rootkit.git
$ cd linux-rootkit
$ And we have a Makefile, life is easy
