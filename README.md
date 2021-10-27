MeshroomCL
==========
MeshroomCL is an extension of the [Meshroom](https://alicevision.org/)
photogrammetry software developed by the AliceVision project. Meshroom
and MeshroomCL provide an interface to algorithms for reconstructing 3D
models from collections of images. While the original Meshroom required
CUDA to achieve accelerated performance, MeshroomCL adds components
based on the OpenCL API and can run on a variety of GPU platforms
(AMD, Intel, NVIDIA, etc.).

Getting Started
---------------
Binary executables for the Windows version of MeshroomCL can be downloaded
from https://github.com/openphotogrammetry/meshroomcl/releases. Download
the file named `MeshroomCL-x.x.x-win64.zip` for the most recent version
of MeshroomCL. After saving and unzipping the zip file, MeshroomCL can
run via the file `Meshroom.exe` inside the containing folder.

Frequently Asked Questions
--------------------------
### Is MeshroomCL available for Linux?

Currently, only Windows binaries are available. However, MeshroomCL can be
run on Linux systems via Wine, by doing the following:
1. Install [Wine](https://www.winehq.org) version 6.5 or later
2. Override Wine's built-in vcomp140.dll by running the [winetricks script](https://wiki.winehq.org/Winetricks) with the command
   `winetricks vcrun2019`. Alternatively, you can obtain a Microsoft-native version of vcomp140.dll and use `winecfg` to configure
   Wine to use it.
