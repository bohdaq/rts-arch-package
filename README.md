## Arch Linux Pacman package for Rust TLS Server

### To install rts as Pacman package:

- Make sure you have Rust and base-devel package installed.

> pacman -S rust
> 
> pacman -S base-devel

- Clone repository

> cd rts-arch-package
> 
> makepkg

- You may need to run commands listed below as an administrator

Replace _VERSION_ with version you've built.

> pacman -U rust-tls-server-_VERSION_.pkg.tar.zst


### Test installation:
> rts

Press Ctrl + C (or CMD + C) to stop server.

### To remove rts:
> pacman -Rs rust-tls-server
