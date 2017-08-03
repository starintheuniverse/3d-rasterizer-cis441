# 3d-rasterizer-cis441
I wrote this program for UO CIS441, Computer Graphics (w/ Prof. Hank Childs).
It takes as input a vector of triangles (vertex locations, vertex colors, vertex normals) + camera and lighting parameters, and renders an image.

I am not uploading my source code publicly, out of respect for the instructor and students in future CIS441 classes.
Please contact me privately if you would like to see the code.

Dependencies & Attributions:
Depends on the VTK library to unpack .vtk geometry files and to export a color buffer to a PNG-formatted file.
Depends on the C++ standard library for memory copy and floating point math.
Prof. Childs supplied inputs and some utility code:
* the polygon geometry (.vtk file);
* lighting parameters;
* a routine to initialize a vector of triangles from a .vtk geometry file;
* a routine to export a color buffer to a PNG file;
* a Triangle struct and a Screen struct (color buffer);
* a Matrix class with a routine to multiply two matrices and a method to act on a point (length-4 float array);
* an animation over the camera parameters;
* custom floating-point rounding procedures;

All other code was written by me by hand.

This program was constructed in iterations, as per the course requirements:
_Phase A_ - Output an image.
_Phase B_ - Basic scanline. Assume 2D flat-bottom triangles (color; vertex locations) with device space coordinates.
_Phase C_ - Introduce arbitrary 2D triangles (color; vertex locations), still device space coordinates.
_Phase D_ - Introduce Z-buffer and 3D triangles (vertex locations & colors) with device space + depth coordinates.
_Phase E_ - Introduce Phong shading, directional lighting. Add vertex normals to triangles.
_Phase F_ - Introduce camera transforms, assume triangle coordinates are in world space.
