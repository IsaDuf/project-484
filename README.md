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
sudo apt-get install libfftw3 # Not Tested
sudo apt-get install cmake # Not Tested
```

Linux Redhat Based:

```bash
sudo yum install fftw-devel # Not Tested
sudo yum install cmake # Not Tested
```

Installing on windows should be possible, but for the time being it is not
supported.

Installing
==========

```bash
mkdir build
cd build
ccmake ../
make
```

Possible Future Dependencies
============================

- libsndfile
