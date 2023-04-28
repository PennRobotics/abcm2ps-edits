QUICK JUMP: [action](https://github.com/PennRobotics/abc2pdf-action) [template](https://github.com/PennRobotics/abc2pdf-template) [abcm2ps-edits](https://github.com/PennRobotics/abcm2ps-edits)



# abcm2ps-edits

The goal of this repository is to discover specific mechanisms in the various
open source ABC parsers and try to bring them into the original _abcm2ps_
source. A secondary goal is to develop a binary with specific functionality in
support of a GitHub Action for converting ABC notation to PDF without the need
of a specific OS, specific programs, or build steps other than copying a
GitHub template.


## TODO

- [ ] fix build scripts and docs (they are currently untested!)
- [ ] time signature using font glyphs
- [ ] other symbols using font glyphs
  - (TODO: add a list of missing/desired symbols here)
- [ ] fix build status link in original **README.md** (using badge on Action script, probably)


The original **README.md** follows:

-----

# abcm2ps

~~[![Build Status](https://travis-ci.org/leesavide/abcm2ps.svg?branch=master)](https://travis-ci.org/leesavide/abcm2ps)~~

### Overview

abcm2ps is a C program which converts music tunes from the ABC music notation
to PostScript or SVG.

Based on [abc2ps](https://github.com/methf/abc2ps),
the Postscript generator for ABC music notation by Michael Methfessel,
it was first developped to print barock organ scores that have independant
voices played on one or many keyboards and a pedal-board
(the 'm' of abcm2ps stands for many or multi staves/voices).
Since this time, it has evolved so it can render many more music kinds.

Note that this program is at end of life. Its successor is
[abc2svg](https://chiselapp.com/user/moinejf/repository/abc2svg).

### Features

The features of abcm2ps are based on the
[ABC draft 2.2 (February 2013)](http://abcnotation.com/wiki/abc:standard:v2.2).
The differences are listed in the
[abcm2ps/abc2svg documentation](http://moinejf.free.fr/abcm2ps-doc/features.html).

### Installation and usage

The installation procedure is described in the file INSTALL.
To build the program with default settings run

```
    ./configure
    make
```

Basically, the program usage is:

    abcm2ps [options] file1 [file1_options] file2 [file2_options] ...

where file1, file2, .. are the ABC input files.
This will generate a Postscript file (default name: `Out.ps`).
Run `abcm2ps -h` to know the list of the command line options.

### Documentation

- abcm2ps.rst describes all command-line options.

  When `abcm2ps` is installed, it may be read by `man abcm2ps`.

- the features and format parameters are described in
    http://moinejf.free.fr/abcm2ps-doc/index.html

### Links

Author's page: http://moinejf.free.fr/

To know more about the ABC music notation, have a look at
    http://abcnotation.com/

Guido Gonzato maintains many abcm2ps binaries and more documentation at
    http://abcplus.sourceforge.net/
