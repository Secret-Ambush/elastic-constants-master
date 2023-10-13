Here's the provided Python code as a Markdown documentation:

```markdown
# castep.py

`castep.py` is a Python script for reading and writing CASTEP (Cambridge Sequential Total Energy Package) files. It provides functionality to extract lattice and atom positions from a CASTEP file, replace the lattice block in a .cell file with a new crystallographic lattice, and extract stress tensor information from a .castep file.

## Usage

### Extract Lattice and Atom Positions

To extract lattice and atom positions from a `.castep` file, you can use the `parse_dotcastep(seedname)` function.

```python
from castep import parse_dotcastep

# Specify the seedname (e.g., "sample") without the file extension
seedname = "sample"

# Extract lattice and atom positions
lattice, pointgroup, atoms = parse_dotcastep(seedname)

# lattice: List of lists representing the 3x3 lattice vectors
# pointgroup: Point group of the crystal
# atoms: List of lists representing atom positions and types
```

### Replace Lattice in .cell File

To replace the lattice block in a `.cell` file with a new crystallographic lattice and add a command to fix the cell during optimization, you can use the `produce_dotcell(seedname, filename, defcell, atoms)` function.

```python
from castep import produce_dotcell

# Specify the seedname (e.g., "sample") without the file extension
seedname = "sample"
# Specify the output filename (e.g., "new_sample.cell")
filename = "new_sample.cell"
# Define the new lattice as a list of lists (3x3 matrix)
defcell = [
    [a11, a12, a13],
    [a21, a22, a23],
    [a31, a32, a33]
]
# List of atoms (if available) to replace in the .cell file
# Set to an empty list if no atom positions need to be replaced
atoms = []

# Replace the lattice block in the .cell file
produce_dotcell(seedname, filename, defcell, atoms)
```

### Extract Stress Tensor

To extract the stress tensor information from a `.castep` file, you can use the `get_stress_dotcastep(filename)` function.

```python
from castep import get_stress_dotcastep

# Specify the filename of the .castep file
filename = "sample.castep"

# Extract stress tensor information
units, stress = get_stress_dotcastep(filename)

# units: String representing the stress units
# stress: Numpy array containing the stress tensor elements
```

## License

This script is provided under the copyright of Andrew Walker (a.walker@ucl.ac.uk) and is for educational and reference purposes. All rights reserved.

For more information and support, please contact the author.
```

This Markdown documentation provides an overview of the `castep.py` script and how to use its functions to work with CASTEP files. You can include this documentation in a README file or any other documentation for your project.
