---
title: Requirements & environment
permalink: /installation/
---

AuriOS is a _freestanding_ kernel: it is built with a cross-compilation
toolchain targeting `i686-elf` and runs inside an emulator.

## Required tools

| Tool                                      | Purpose                          |
| ----------------------------------------- | -------------------------------- |
| `i686-elf-gcc`                            | Cross-compiler (i686-elf target) |
| `i686-elf-ld`                             | Cross linker                     |
| `nasm`                                    | Assembler (Netwide Assembler)    |
| `qemu-system-i386` / `qemu-system-x86_64` | Emulator to test the kernel      |
| `make`                                    | Build automation                 |
| `grub-mkrescue`, `xorriso`, `mtools`      | Bootable ISO image generation    |

> If `i686-elf-gcc` is not found, the `Makefile` automatically falls back to the
> host `gcc` with `-m32` flags. A proper cross toolchain is still recommended.

## Install dependencies

The `Makefile` provides cross-distribution install target:

```bash
make install    # Linux / Unix
```

## Get the source code

```bash
git clone {{ site.repo_url }}.git
cd aurios
```

Once your environment is ready, move on to
[building & running](/building/).
