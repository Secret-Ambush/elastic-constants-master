This Python script, `rotCij.py`, is designed to rotate a 6x6 matrix representation of an elastic constants tensor around one of three axes (x, y, or z) by a specified angle in radians. It also includes a command-line interface for testing and usage. Here's an explanation of the code:

1. The script begins with a brief docstring, specifying its name and purpose, and includes the copyright information.

2. `import numpy as np`: Imports the NumPy library with the alias `np` for numerical calculations.

3. `version = 0.1`: Defines a version number for the script.

4. The `_rotMat6` function is defined to calculate the 6x6 rotation matrix for the given axis (0, 1, or 2) and angle in radians. This function performs rotations in 3D space.

5. `rotCij` is a function that rotates an input 6x6 elastic constants tensor around a specified axis by a specified angle. It uses the `_rotMat6` function to calculate the rotation matrix. The output is a rotated tensor.

6. The `if __name__ == '__main__':` block is used to run the script as a standalone program when executed, not when imported as a module.

7. The script reads command-line arguments, including the rotation axis, rotation angle (in radians), and the input file containing the 6x6 elastic constants tensor.

8. It calls the `rotCij` function to rotate the tensor.

9. It then prints the input matrix, the rotation angle, and the output matrix, each formatted for better readability.

10. If a fifth command-line argument is provided, it saves the rotated matrix to the specified file.

In summary, this script provides a utility for rotating 6x6 elastic constants tensors by a specified angle around one of three axes (x, y, or z). It can be used for various purposes, such as material science simulations, where the orientation of the crystal lattice or material properties may change due to external factors or transformations.
