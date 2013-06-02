Project 484
===========

Dependencies
============

- FFTW3
- Cmake

Clone the repo, cd to that directory.

OSX:

If you use homebrew the dependancies can be installed by:

```bash
brew install fftw
brew install cmake
```

Linux Debian Based:

```bash
apt-get install fftw # Not Tested
```

Linux Redhat Based:

```bash
yum install fftw # Not Tested
```

Installing on windows should be possible, but for the time being it is not
supported.

Installing
==========

```bash
touch build
cd build
ccmake ../
make
```

Possible Future Dependencies
============================

- libsndfile
