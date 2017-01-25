GFXMath README

Submitted By		: Jose Vicente D. Chan Jr.
Campus Wide ID		: 892984154
Class			: CPSC 484
Time			: Tue & Thu @ 1:00PM

Assignment 3 -- Implementing a Matrix class

Summary:

GFXMath.h now contains a template for the implementation of a matrix class, in addition to the vector class.
	The following matrix operations are implemented and are succcessfully working via the use of
	GFXMath_Test program.

Addition	 	- The "+" operator has been overloaded in order to make matrix addition possible. 
		   	Returns: MatNM object.
Subtraction	 	- The "-" operator has been overloaded for matrix subtraction.
		   	Returns: MatNM object.
Multiplication s	- The "*" is also overloaded to make the multiplication of a scalar and matrix possible.
		   	Returns: MatNM object.
Multiplication M	- The "*" is also overloaded to get the product of two same size matrices.
			Returns: MatNM object. 
Division	 	- The "/" is overloaded for division of a matrix and a scalar.
		   	Returns: MatNM object. 
Unary Minus		- The "-" has also been overloaded to convert a matrix's components to negative and vice-versa.
		   	To use this operator, it will have to be -<myMatrixObject>
		   	Returns: MatNM object.
Boolean Equals	 	- The "==" operator has been overloaded to check for equality of two matrices.
		   	Returns: A boolean value.
Boolean Not Equals  	- The "!=" operator has also been overloaded to check for the inequality of two matrices.
			Returns: A boolean value.
Transpose		- The transpose() method inside the MatNM class will get the transpose of the matrix object.
			Returns: A MatNM object.
Identity 		- Inside the MatN child class, the identity() method can be called to spit out an identity matrix.
			Returns: A ManN object.

For the TMat2, TMat3, and TMat4 square matrix child classes, the following methods have been implemented
and are working in accordance to the GFXMath_Test program:

Determinant		- Each of the TMatN classes can calculate the determinant of their respective square matrix.
			Returns: A value of type T
Minor			- Each of the TMatN classes can calculate the minor that is specified by column and row 
			of their respective matrix.
			Returns: A value of type T
Cofactor		- Each of the TMatN classes can also the get cofactor of their respective square matrix.
			Returns: A value of type T
Adjugate		- Each of the TMatN classes can also get the their adjugate matrix.
			Returns: A TMatN object.
Inverse			- Eacf of the above classes can also calculate their inverse matrix.
			Returns: A TMatN object.

An additional file is also included with this submission, GFXMath_Test.cpp is a unit test for the template in order to check
if all the Matrix classes and its methods was properly implemented.


Building:

To compile the program, run `make' on OS X and Linux or `gmake' on FreeBSD. The Makefile is compatible with GNU Make and not BSD Make. The list of make targets are:
 . all         build all (default)
 . clean       remove intermediate files, core files, backup files
 . spotless    clean + remove all dependency files

The build depends on the PThreads library and the Google Test library. Pthreads is typically included with your development environment and the Google Test libraries are included in the Titan OpenGL Kit.

**TLA VM Users: Release 20150119 is missing the Google Test libraries but
includes the header files and source code. TLA VM release 20150125 has the library correctly installed.**
