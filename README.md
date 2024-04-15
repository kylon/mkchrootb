mkchrootb

chroot-only AUR helper written in bash ([AUR package](https://aur.archlinux.org/packages/mkchrootb))

features:
- chroot-only
- local repo for AUR pkgs
- pkgs and db signing
- view/edit pkgs before build
- local repo and chroot management
- local repo pkgs update
- build local PKGBUILDs
- build pkgs that require X11 access

not available:
- dependency solver (build and add to local repo dependencies before the pkg build)


a \[aur\] local repo will be created

pacman.conf and makepkg.conf from installed os will be copied to chroot, each time chroot is created

```
Usage: mkchrootb [options]

options:
-c
    clean cache

-cr
    clean local repo

-co
    clean local repo old pkgs

-cc
    clean cache and rebuild chroot

-p pkg[,pkg2,pkg3,..]
    install pkgs to chroot, comma separated list (official or local repo)

-a pkg[,pkg2,pkg3,..]
    build pkgs from aur, comma separated list

-d pkg[,pkg2,pkg3,..]
    uninstall pkgs, comma separated list

-da pkg[,pkg2,pkg3,..]
    delete pkgs from local repo database, comma separated list

-l
    build PKGBUILD in current path

-x
    enable access to X server to build pkgs that run GUIs in build process

-r
    add pkgs to local repo after build

-i
    install pkgs after build

-u
    update pkgs in local repo

-w
    ask to view/edit PKGBUILD before build (vifm > nano > vi, first one found in that order)

-k
    do not remove package repo from cache folder (deleted by default after build)

-ss
    create mkchrootb signing key

-s
    sign database and pkgs

-us
    remove database and pkgs signature

-h
    this help
```
