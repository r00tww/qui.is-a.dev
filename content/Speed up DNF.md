---
title: Speed up DNF
---
DNF is very slow without modifying `dnf.conf`. We'll modify `/etc/dnf/dnf.conf` for speed up DNF.

# Dependencies
```
deltarpm
```

# DNF.conf

Add these to `/etc/dnf/dnf.conf`:

```sh
# dnf.conf
fastestmirror=true
max_parallel_downloads=20
deltarpm=true
```

By the way, you can add `defaultyes=true` for `[Y/n]` (default is `[y/N]`) in package installs.

