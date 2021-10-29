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
the file named `MeshroomCL-x.y.z-win64.zip` for the most recent version
of MeshroomCL. After saving and unzipping the zip file, MeshroomCL can be
run via the file `Meshroom.exe` inside the containing folder.

After running MeshroomCL, follow these basic steps to reconstruct a 3D model
from a set of images:
1. Load your images into MeshroomCL by either dragging the files into the Images
pane (upper left) or by using the _File &rarr; Import Images_ menu option to select
them.
2. Click the green _Start_ button at the top center of the MeshroomCL window.
3. You will be prompted to save your project. Select _Save_ and specify
a project filename (all project files will be stored in a sub-folder here).
4. Click the green _Start_ button again. Processing will begin.
5. You can monitor the progress of the processing by observing the colored
bars at the top of the MeshroomCL window and within each individual node
(green="finished", orange="in progress", blue="pending", red="error").
6. When the StructureFromMotionCL node has finished processing, the computed
camera positions and sparse point cloud will be automatically displayed in the
3D Viewer pane.
7. As each node finishes processing, you can double-click on that node to
view its result in the 3D Viewer pane.
8. When the last node (TexturingCL) finishes, you can double-click on the node
to view the textured 3D model in the 3D Viewer pane, or right-click on the node
and select _Open Folder_ to access the 3D model files.

Frequently Asked Questions
--------------------------
### Is MeshroomCL available for Linux?

Currently, only Windows binaries are available. However, MeshroomCL can be
run on Linux systems via Wine, by doing the following:
1. Install [Wine](https://www.winehq.org) version 6.5 or later
2. Override Wine's built-in vcomp140.dll by running the [winetricks script](https://wiki.winehq.org/Winetricks) with the command
   `winetricks vcrun2019`. Alternatively, you can obtain a Microsoft-native version of vcomp140.dll and use `winecfg` to configure
   Wine to use it.
