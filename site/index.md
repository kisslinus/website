---
title: KISS
---

An independent Linux® distribution with a focus on [simplicity](#simplicity) and the concept of ["less is more"](#less-is-more). The distribution targets **only** the x86-64 architecture and the English language.


## Overview

- Uses a plain-text [package system](/package-system.txt) which is **language agnostic** and parseable with basic UNIX utilities.

- Uses a [package manager](https://github.com/kisslinux/kiss) written in **600~ lines** of POSIX sh (*excluding blank lines and comments*).

- Based on [musl libc](https://www.musl-libc.org/), [busybox](https://busybox.net/) and the [Linux kernel](https://kernel.org).

- All shell code is linted by and passes [shellcheck](https://www.shellcheck.net/) (*including each and every repository package*).

- All packages are **compiled from source** by the package manager which automatically handles dependencies, patches, etc.

- Explicitly **excludes** the following software: dbus, systemd, polkit, gettext, intltool, pulseaudio, pam, wayland, logind, ConsoleKit2 and all Desktop Environments. See [Philosophy](#philosophy).

- **Choice!** The coreutils, init, device manager, compiler, shell and \* can be replaced. There's no lock-in to specific software (excluding `musl` and the kernel of course).

- Rootless [Xorg](https://x.org) environment **without** any additional software.

- Repository signing through [git](https://git-scm.com/) and [gnupg](https://www.gnupg.org/) (*based on signed commits and built into git itself*).


## Philosophy

See: <https://k1ss.org/guidestones.txt>

### Simplicity

This distribution follows the [KISS principle](https://en.wikipedia.org/wiki/KISS_principle) (*Keep it Simple Stupid*).

A distribution being "simple" has many different interpretations. It may mean simple to use, simple to develop or simple in its implementation. Further, the phrase "simple to use" may differ from person to person.

Users with prior knowledge of Linux and basic programming skills will find this distribution simple in all three examples given above. A user without prior knowledge may see this distribution as the exact opposite.

The more code and documentation one adds to a project, the more time it takes to maintain it and the risk of things going awry rises. Code *is* weight and the focus should be on keeping it light.

### Less is more

This distribution uses less software where possible and follows the belief that the less software and code running the less error prone the system will be overall.

The absence of software from the repositories does **not** mean it cannot be installed. Any user can further package whatever is preferred, else use third-party repositories.

It is easier to **add** things to a system than it is to **remove** them. Providing only a minimal base, users can then extend this distribution to meet their individual needs.


## Further reading

See: <https://k1ss.org/guidestones.txt>

- [Install KISS](/pages/install)
- [Package System](/package-system.txt)
