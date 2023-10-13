# rotVec.py

This Python script provides functions for rotating 3-element vectors around different axes. It is used to manipulate lattice vectors in the context of crystallography and materials science. The script also imports external functions from `rotCij.py` and `generate_strain.py`.

## Functions

1. `_rotMat3(axis, theta)`: Constructs a 3x3 rotation matrix for rotating a vector around a specified axis by a given angle in radians.
   - `axis`: The rotation axis (0 for X, 1 for Y, 2 for Z).
   - `theta`: The rotation angle in radians.
   - Returns a 3x3 rotation matrix.

2. `rotVec(inVec, axis, theta)`: Rotates a 3-element vector around an axis (X, Y, or Z) by a specified angle in radians.
   - `inVec`: The input 3-element vector to be rotated.
   - `axis`: The rotation axis (0 for X, 1 for Y, 2 for Z).
   - `theta`: The rotation angle in radians.
   - Returns the rotated 3-element vector as a numpy array.

## Usage

You can use the provided functions to perform vector rotations around different axes. The script also includes a main block that demonstrates how to use these functions. It reads lattice parameters and a matrix from a file, performs rotations to align the lattice vectors, and calculates angles.

## Dependencies

This script depends on external functions from `rotCij.py` and `generate_strain.py`. Ensure that these dependencies are properly installed and accessible when using this script.

## Running the Script

To run the script, provide the necessary input arguments when executing it. For example:

```shell
python rotVec.py 10 10 10 90 90 120 input_file.txt
```

This will perform vector rotations based on the input arguments and print the results to the console.

Make sure to have the required dependencies and the appropriate input file to use this script effectively.

Note: This documentation provides an overview of the script and its usage. Additional details about the behavior and specific use cases are not included here.


This documentation provides an overview of the script's purpose, the functions it provides, usage instructions, and its dependencies. Users can refer to this documentation to understand how to use the script and its functionality.
