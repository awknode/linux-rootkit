# linux-rootkit

# Hooks the LKM and bypasses ASLR, DEP, NX bit, Canaries, etc mostly with gadget and ROP chains but other tricks are involved. We also move glibc to the side as well, he is not needed.
# Kernel <-> Userland
# Ring0


# linux rookit

Hooks the LKM and bypasses ASLR, DEP, NX bit, Canaries, etc mostly with gadgets and ROP chains but other tricks are involved. We also move glibc to the side as well, he is not needed.

## About

This attacks multiple architectures, years went into this project.

### Installation

```bash
# Commands
$ git clone https://github.com/awknode/linux-rootkit.git
$ cd linux-rootkit
$ compile
