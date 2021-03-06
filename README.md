# Introduction

This page contains software and instructions for
[a GUI interface](http://www.f-zhou.com/mocgui_code.html) for viewing
motion capture data.


# Installation

1. Download the code via `git clone https://github.com/zhfe99/mocgui.git` or from this [link](https://github.com/zhfe99/mocgui/archive/master.zip);
2. Set `mocgui/` as the current folder in Matlab;
3. Run `addPath` in Matlab to add sub-directories into the path of Matlab.
4. Run `mocgui` or `demoMoc` in Matlab.


# Instructions

The package of `mocgui.zip` contains the following files and folders:
- `./data`: This folder contains a subset of the [CMU Motion Capture dataset](http://mocap.cs.cmu.edu).
- `./src`: This folder contains the main implementation of the GUI interface.
- `./lib`: This folder contains some necessary library functions.
- `./addPath.m`: Adds the sub-directories into the path of Matlab.
- `./mocgui.m`: The interface function.
- `./mocgui.fig`: The Matlab fig file to save the window configuration.
- `./demoMoc.m`: A demo file for loading and visualizing motion capture data.


# FAQs
### How to load more data?
- All the mocap data are located under `data/cmu`. In this package, I
  have put a folder `data/cmu/S02` containing all the sequences
  performed by subject S02. You can download more data from the website of
  the [CMU Motion Capture dataset](http://mocap.cs.cmu.edu) and put the files in a similar structure as the
  folder `data/cmu/S02`.

### How to show one frame of a mocap data?
- At the end of `demoMoc.m`, you can find an example of showing one frame of a mocap data.

### How to get the coordinate of a mocap data?
- The function `cmuMoc` creates a structure variable named `wsMoc`,
  which contains all the mocap data for one sequence. In particular,
  `wsMoc.QC` is a `3 x nJ x nF` matrix, containing the 3D coordinate
  of `nJ` joints of a `nF`-length motion capture data. You can check
  the code `demoMoc.m` for the example.


# Copyright
This software is free for use in research projects. If you publish
results obtained using this software, please use this citation.

    @article{ZhouDH13,
        author    = {Feng Zhou and Fernando {De la Torre} and Jessica K. Hodgins},
        title     = {Hierarchical Aligned Cluster Analysis for Temporal Clustering of Human Motion},
        journal   = {IEEE Transactions Pattern Analysis and Machine Intelligence (PAMI)},
        year      = {2013},
        volume    = {35},
        number    = {3},
        pages     = {582-596},
    }

If you have any question, please feel free to contact Feng Zhou (zhfe99@gmail.com).
