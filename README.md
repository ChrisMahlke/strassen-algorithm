# Matrix Operations

This program provides a way to represent square matrices and perform basic matrix operations. The primary operations supported are addition, subtraction, multiplication, and submatrix extraction.

## Code Structure

1. **Header File** (`matrix.h`):
    - Defines the `Matrix` class that holds the details and operations of the square matrices.
    - Member functions include:
        - Basic constructors and destructors.
        - Overloaded operators for input/output.
        - Arithmetic operations such as addition, subtraction, and multiplication.
        - Submatrix extraction.
    - Note: Matrix dimensions are assumed to be powers of 2 for simplicity.

2. **Implementation File 1** (`matrix.cpp`):
    - Implements all the member functions and constructors defined in the `Matrix` class.
    - This file also provides utility functions, for example, `ceilLogAndCompute`, to ensure matrix sizes are powers of 2.

3. **Implementation File 2** (`main.cpp`):
    - Contains a simple matrix multiplication benchmark (`matmultNaive`) which multiplies two square matrices using a direct O(n^3) method.
    - Also uses an `IPM_timer` to measure the performance of this naive matrix multiplication.
    - Main function (`main`) reads the size of the matrix from command line arguments and then multiplies two matrices of the given size.

## How to Run

1. **Compilation**:
   Ensure you have all required dependencies, especially the `ipm-2.0a/IPM_timer.h` header. Once done, you can compile the project with:

   ```
   g++ matrix.cpp main.cpp -o matrix_operations
   ```

   This will create an executable named `matrix_operations`.

2. **Usage**:
   Run the executable with the size of the matrix (a power of 2) as an argument. For example:

   ```
   ./matrix_operations 4
   ```

   This command will multiply two 4x4 matrices and display the results along with the time taken.

## Notes

- All matrices are assumed to be square.
- The size of the matrix is expected to be a power of 2 due to certain optimization techniques applied in the `Matrix` class.
- Matrix multiplication uses the conventional O(n^3) approach.
- Ensure proper error handling when reading input from files or the command line.

## Example

Running:

```
./matrix_operations 2
```

Will yield something like:

```
*************
* Matrix 1  *
*************
1.0 1.99
1.0 1.99

*************
* Matrix 2  *
*************
1.0 1.99
1.0 1.99

************
* Product: *
************
2.99 5.9601
2.99 5.9601

Elapsed time to compute: [Some value]u
MFlops: [Some value]
```

---

This README provides a comprehensive understanding of the code and its execution. Make sure to adjust paths and filenames accordingly if any changes are made to the codebase.
