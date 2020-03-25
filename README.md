# imagedecoder.mpo addon for Kodi

This is a [Kodi](http://kodi.tv) image decoder addon for MPO images.

[![License: GPL v2+](https://img.shields.io/badge/License-GPL%20v2+-blue.svg)](LICENSE.md)
[![Build Status](https://travis-ci.org/xbmc/imagedecoder.mpo.svg?branch=master)](https://travis-ci.org/xbmc/imagedecoder.mpo)
[![Build Status](https://dev.azure.com/teamkodi/binary-addons/_apis/build/status/xbmc.imagedecoder.mpo?branchName=Leia)](https://dev.azure.com/teamkodi/binary-addons/_build/latest?definitionId=27&branchName=Leia)
[![Build Status](https://jenkins.kodi.tv/view/Addons/job/xbmc/job/imagedecoder.mpo/job/Leia/badge/icon)](https://jenkins.kodi.tv/blue/organizations/jenkins/xbmc%2Fimagedecoder.mpo/branches/)

## Build instructions

When building the addon you have to use the correct branch depending on which version of Kodi you're building against.
If you want to build the addon to be compatible with the latest kodi `master` commit, you need to checkout the branch with the current kodi codename.
Also make sure you follow this README from the branch in question.

### Linux

The following instructions assume you will have built Kodi already in the `kodi-build` directory 
suggested by the README.

1. `git clone --branch Leia https://github.com/xbmc/xbmc.git`
2. `git clone https://github.com/xbmc/imagedecoder.mpo.git`
3. `cd imagedecoder.mpo && mkdir build && cd build`
4. `cmake -DADDONS_TO_BUILD=imagedecoder.mpo -DADDON_SRC_PREFIX=../.. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../../xbmc/kodi-build/addons -DPACKAGE_ZIP=1 ../../xbmc/cmake/addons`
5. `make`

The addon files will be placed in `../../xbmc/kodi-build/addons` so if you build Kodi from source and run it directly 
the addon will be available as a system addon.
