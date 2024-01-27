# simplex_3d-
3D Simplex noise abstraction for Pure Data (Pd) with signal rate input/output (based on Ken Perlin's successor to "Perlin noise")

Patch is mainly adapted from the Java code in https://weber.itn.liu.se/~stegu/simplexnoise/simplexnoise.pdf

## Installation
Install by adding the downloaded folder as `simplex_3d~/` to Pd's path (e.g. in `externals` directory).

## Usage
The abstraction `simplex_3d~` requires the number of octaves as its first argument (it will default to 1 - but produce a clone error message).

Additional optional arguments:
* `normalize` or `n` flag to ensure that the sum of all octaves will not exceed 1.
* `-persistence` or `-p` parameter to set persistence (values < 1 will attenuate higher octaves, values > 1 will amplify them).
* `-seed` or `-s` parameter to initialize the gradient vector permutation with a given seed value. Without a value, the permutation gets reseeded randomly.
* `-offset` or `-o` parameter to set initial offset for x, y and z coordinates (useful if only one axis is used for input since values along 0-coordinates create a less noisy pattern).

Inlets are:
1. x-coordinate
2. y-coordinate
3. z-coordinate
4. persistence

*Help patch is currently missing*
