# mimic-english

English language support for mimic

This mimic plugin provides English language analysis support to mimic.

It is based on the usenglish flite module, the cmu lexicon (cmulex) and Amepd (The
american pronounciation dictionary).

## Dependencies:

### Mimic core:

Install mimic-core from https://github.com/zeehio/mimic-core first.

### Meson and ninja

#### Windows

- [python3](https://www.python.org/downloads/windows/)
- [ninja](https://github.com/ninja-build/ninja/releases)
- meson: `pip install meson` (once python is installed)

#### OSX:

brew install python3 ninja pkg-config
pip3 install --user meson

#### Linux

##### On Debian/Ubuntu
```
$ sudo apt-get install python3 python3-pip gcc pkg-config ninja-build
```

##### On Fedora
```
$ sudo dnf install python3 python3-pip gcc pkgconfig ninja-build
```

##### On Arch
```
$ sudo pacman -S --needed install python python-pip gcc pkg-config ninja
```

## Installation

If mimic-core has been installed to a custom prefix, please export the pkg-config path:

- `export PKG_CONFIG_PATH="/path/to/mimic-core/prefix/lib/x86_64-linux-gnu/pkgconfig"`

Then build and install mimic-english:

- `meson builddir --prefix="/path/to/mimic-core/prefix/"`
- `ninja -C builddir test`
- `ninja -C builddir install`


