# SimulIDE for FreeBSD

FreeBSD port of SimulIDE 1.1.0-SR2, tested on FreeBSD 15.1 amd64.

Includes native FreeBSD build, Qt 5 dependencies, desktop entry, icon, data and examples.

## Build

```sh
cd freebsd/ports/simulide
make package
```

Install:

```sh
sudo pkg install ./work/pkg/simulide-1.1.0.pkg
```

## Licenses

SimulIDE source code: GNU AGPL-3.0 (`COPYING`).

FreeBSD packaging and integration files: BSD 3-Clause (`LICENSE-BSD-3-Clause.txt`).
