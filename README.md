## Arch Linux Pacman package for Rust TLS Server

### To install rts as Pacman package:

#### 1. Install rust

> pacman -S rust

#### 2. Install required build tools
> pacman -S base-devel

#### 3. Build from source
> cd ~

> mkdir git

> cd git

> git clone https://github.com/bohdaq/rts-arch-package.git

> cd rts-arch-package

> makepkg

#### 4. Install 
> ls -l

Replace _VERSION_ with version you've built.

> sudo pacman -U rust-tls-server-_VERSION_.pkg.tar.zst


### Test installation:

> rts

Press Ctrl + C (or CMD + C) to stop server.

### To remove rts:

> pacman -Rs rust-tls-server
