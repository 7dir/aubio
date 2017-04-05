aubio
=====

[![Travis build status](https://travis-ci.org/aubio/aubio.svg?branch=master)](https://travis-ci.org/aubio/aubio "Travis build status")
[![Appveyor build status](https://img.shields.io/appveyor/ci/piem/aubio/master.svg)](https://ci.appveyor.com/project/piem/aubio "Appveyor build status")
[![Landscape code health](https://landscape.io/github/aubio/aubio/master/landscape.svg?style=flat)](https://landscape.io/github/aubio/aubio/master "Landscape code health")
[![Documentation Status](https://readthedocs.org/projects/aubio/badge/?version=latest)](http://aubio.readthedocs.io/en/latest/?badge=latest "Documentation status")
[![Commits since last release](https://img.shields.io/github/commits-since/aubio/aubio/0.4.4.svg)](https://github.com/aubio/aubio "Commits since last release")
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.438682.svg)](https://doi.org/10.5281/zenodo.438682)

aubio is a library to label music and sounds. It listens to audio signals and
attempts to detect events. For instance, when a drum is hit, at which frequency
is a note, or at what tempo is a rhythmic melody.

Its features include segmenting a sound file before each of its attacks,
performing pitch detection, tapping the beat and producing midi streams from
live audio.

aubio provide several algorithms and routines, including:

  - several onset detection methods
  - different pitch detection methods
  - tempo tracking and beat detection
  - MFCC (mel-frequency cepstrum coefficients)
  - FFT and phase vocoder
  - up/down-sampling
  - digital filters (low pass, high pass, and more)
  - spectral filtering
  - transient/steady-state separation
  - sound file read and write access
  - various mathematics utilities for music applications

The name aubio comes from _audio_ with a typo: some errors are likely to be
found in the results.

Python module
-------------

A python module for aubio is provided. For more information on how to use it,
please see the file [`python/README.md`](python/README.md) and the
[manual](https://aubio.org/manual/latest/) .

Examples tools
--------------

A few simple command line tools are included along with the library:

 - `aubioonset` outputs the time stamp of detected note onsets
 - `aubiopitch` attempts to identify a fundamental frequency, or pitch, for
   each frame of the input sound
 - `aubiomfcc` computes Mel-frequency Cepstrum Coefficients
 - `aubiotrack` outputs the time stamp of detected beats
 - `aubionotes` emits midi-like notes, with an onset, a pitch, and a duration
 - `aubioquiet` extracts quiet and loud regions

Additionally, the python module comes with the following script:

 - `aubiocut` slices sound files at onset or beat timestamps

The latest version of the documentation can be found at:

  https://aubio.org/documentation

Build Instructions
------------------

aubio compiles on Linux, Mac OS X, Windows, Cygwin, and iOS.

To compile aubio, you should be able to simply run:

    make

To compile the python module:

    ./setup.py build

See also the [manual](https://aubio.org/manual/latest/) for more information
about [installing aubio](https://aubio.org/manual/latest/installing.html).

Credits and Publications
------------------------

This library gathers music signal processing algorithms designed at the Centre
for Digital Music and elsewhere. This software project was developed along the
research I did at the Centre for Digital Music, Queen Mary, University of
London. Most of this C code was written by myself, starting from published
papers and existing code. The header files of each algorithm contains brief
descriptions and references to the corresponding papers.

Special thanks go Juan Pablo Bello, Chris Duxbury, Samer Abdallah, Alain de
Cheveigne for their help and publications. Also many thanks to Miguel Ramirez
and Nicolas Wack for their bug fixing.

Substantial informations about the algorithms and their evaluation are gathered
in:

  - Paul Brossier, _[Automatic annotation of musical audio for interactive
    systems](https://aubio.org/phd)_, PhD thesis, Centre for Digital music,
Queen Mary University of London, London, UK, 2006.

Additional results obtained with this software were discussed in the following
papers:

  - P. M. Brossier and J. P. Bello and M. D. Plumbley, [Real-time temporal
    segmentation of note objects in music signals](https://aubio.org/articles/brossier04fastnotes.pdf),
in _Proceedings of the International Computer Music Conference_, 2004, Miami,
Florida, ICMA

  -  P. M. Brossier and J. P. Bello and M. D. Plumbley, [Fast labelling of note
     objects in music signals] (https://aubio.org/articles/brossier04fastnotes.pdf),
in _Proceedings of the International Symposium on Music Information Retrieval_,
2004, Barcelona, Spain


Contact Info and Mailing List
-----------------------------

The home page of this project can be found at: https://aubio.org/

Questions, comments, suggestions, and contributions are welcome. Use the
mailing list: <aubio-user@aubio.org>.

To subscribe to the list, use the mailman form:
https://lists.aubio.org/listinfo/aubio-user/

Alternatively, feel free to contact directly the author.


Copyright and License Information
---------------------------------

Copyright (C) 2003-2016 Paul Brossier <piem@aubio.org>

aubio is free software: you can redistribute it and/or modify it under the
terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.
