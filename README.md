# linux-rootkit
 Kernel <-> Userland
 Ring0

Hooks the LKM and bypasses ASLR, DEP, NX bit, Canaries, etc mostly with gadgets and ROP chains but other tricks are involved. We also move glibc to the side as well, he is not needed. C&C can be setup to utilize this bot later on for whatever you may need, we did this back in 2008-2013 and many other barriers involved. Wouldn't be hard to get it back working, just need to update the sysclone.d offsets and elf headers, also arent we using FASM now and not ASLR? I'm out of the loop, not a problem but this was just educational. Hope someone gets something out of it

## About

This attacks multiple architectures with vmalloc() -> kmem() and kmem() -> tricks (ask me more) 

### Installation

```bash
# Commands
$ git clone https://github.com/awknode/linux-rootkit.git
$ cd linux-rootkit
$ And we have a Makefile, life is easy
