# Ambisonic Toolkit Matrices

A set of matrix files for matrix encoders and decoders.


## Matrix formats

Each matrix is provided in several formats:

***.txt**

A text file containing the matrix, with one row per line, and cell values separated by spaces. Refer to [acn-n3d1.txt](FOA/decoders/acn-n3d1.txt) for an example.

***.mosl.txt**

A text file containing one cell value per line. The first two values gives the dimension of the matrix as number of rows and number of columns. Empty lines can be used for improved readability. Comment lines can be added, starting with `//`. Imline comments are also supported. Refer to [acn-n3d1.mosl.txt](FOA/decoders/acn-n3d1.mosl.txt) for an example.

## Using the matrices

### Using Matrices with Reaper

The kernels are included as part of the [ATK for Reaper](http://ambisonictoolkit.github.io/download/reaper/) install, and there is no need to download and install the kernels seperately.


### Using Matrices with SuperCollider

Information is forthcoming.