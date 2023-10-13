# concat_cij_latex.py

`concat_cij_latex.py` is a Python script for widening a LaTeX table by adding additional data from another LaTeX table. This can be useful when you want to concatenate or add rows from one LaTeX table to another.

## Usage

To use this script, follow the instructions below.

1. Make sure you have two LaTeX tables that you want to concatenate. One is the left table, and the other is the right table. Save these tables in separate text files.

2. Run the `latex_table_cocat(left_file, right_file, out_file=None)` function, specifying the file paths for the left and right tables. You can optionally provide an `out_file` parameter to specify the output file. If `out_file` is not provided, the left file will be overwritten with the widened table.

```python
from concat_cij_latex import latex_table_cocat

# Specify the file paths for the left and right tables
left_file = "left_table.tex"
right_file = "right_table.tex"

# Specify an output file (optional, if not provided, left_file will be overwritten)
out_file = "output_table.tex"

# Concatenate the tables
latex_table_cocat(left_file, right_file, out_file)
```

3. The script reads the tables line by line and combines them into a new table, ensuring that the rows align correctly. The result is saved to the output file or overwrites the left table.

## License

This script is provided under the copyright of Andrew Walker and is for educational and reference purposes. All rights reserved.

For more information and support, please contact the author.

This Markdown documentation provides an overview of the `concat_cij_latex.py` script and how to use it to concatenate LaTeX tables. You can include this documentation in a README file or any other documentation for your project.
