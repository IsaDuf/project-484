This Project Still Needs A Name
===============================

Dependencies
============

- FFTW3
- Cmake

Clone the repo, cd to that directory.

OSX:

If you use homebrew the dependancies can be installed by:

```bash
brew install fftw
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
```

Possible Future Dependencies
============================

- libsndfile
