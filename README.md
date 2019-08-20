# Matrix Ops (UNIX)

> CS-344 (Operating Systems I) Program

A series of matrix operations written in UNIX.

## How to compile and run:
> 1. Copy/paste all program code into a directory
> 2. In that directory, type the command: `chmod +x generate` to make *generate* function executable  
> 3. Type the command: `chmod +x matrix` to make *matrix* function executable
> 4. Create two (or more) matrices. This can be done by:
> - Typing the command: `generate x y 10` , where x and y are the  number of rows and columns (respectively) you want your matrix to be, and `m1` is the name of the file where it will be stored  
> **or**  
> - Making your own custom matrix inside a file (columns must be tab separated, and rows must end with a newline character)  

> Once you have at least two matrices in files, you man run any of the following commands:
> - `matrix dims [MATRIX]`, where MATRIX is the name of some matrix file  
> - `matrix transpose [MATRIX]`, where MATRIX is the name of some matrix file  
> - `matrix mean [MATRIX]`, where MATRIX is the name of some matrix file  
> - `matrix add [MATRIX_LEFT] [MATRIX_RIGHT]`, where MATRIX_LEFT and MATRIX_RIGHT are two matrix files  
> - `matrix multiply [MATRIX_LEFT] [MATRIX_RIGHT]`, where MATRIX_LEFT and MATRIX_RIGHT are two matrix files  

## Example run:
> `$ cat m1`  
> 1   2	  3	  4  
> 5	  6 	7	  8  
> `$ cat m2`  
> 1 	2  
> 3	  4  
> 5 	6  
> 7 	8  
> `$ matrix dims m1`  
> 2   4  
> `$ cat m2 | matrix dims`  
> 4   2  
> `$ matrix add m1 m1`  
> 2	  4	  6	  8  
> 10	12	14	16  
> `$ matrix add m2 m2`  
> 2	  4  
> 6	  8  
> 10	12  
> 14	16  
> `$ matrix mean m1`  
> 3	  4	  5	  6  
> `$ matrix transpose m1`  
> 1	  5  
> 2	  6  
> 3	  7  
> 4	  8  
> `$ matrix multiply m1 m2`  
> 50	  60  
> 114	  140  

## Concepts learned/used:
> - UNIX shells  
> - UNIX commands
> - Input/output redirecton
> - UNIX piping
> - Subshells
> - Directories, files, and permissions
> - VIM
