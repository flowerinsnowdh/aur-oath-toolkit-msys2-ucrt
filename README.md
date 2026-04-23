AUR of the [oath-toolkit](https://archlinux.org/packages/extra/x86_64/oath-toolkit/) package in environment [MSYS2](https://www.msys2.org/)

# Usage
## Clone the repository
```shell
git clone https://github.com/flowerinsnowdh/aur-oath-toolkit-msys2-ucrt.git
```

## Install the PGP key of upstream

[B1D2BD1375BECB784CF4F8C4D73CF638C53C06BE](https://keys.openpgp.org/vks/v1/by-fingerprint/B1D2BD1375BECB784CF4F8C4D73CF638C53C06BE)

```shell
gpg --search-keys B1D2BD1375BECB784CF4F8C4D73CF638C53C06BE
```

## Build
```shell
makepkg
```

## Install
```shell
pacman -U oath-toolkit-msys2-ucrt-2.6.14-1-x86_64.pkg.tar.zst
```
