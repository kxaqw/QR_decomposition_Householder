# QR_decomposition_Householder

## 📌 Description

This project provides a from-scratch implementation of **QR decomposition** using **Householder reflections**, a numerically stable and efficient method for decomposing a given matrix `A` into an orthogonal matrix `Q` and an upper triangular matrix `R`, such that:

Unlike typical implementations that rely on high-level libraries like `numpy.linalg`, this version manually constructs each Householder matrix and performs all vector and matrix operations step by step. This approach helps in gaining a deeper understanding of the underlying linear algebra and transformation mechanics involved in QR decomposition.

The code includes:
- A safe implementation of vector and matrix operations
- Construction of Householder matrices
- QR decomposition with intermediate steps
- Rigorous verification of the decomposition
- File I/O to read input matrices and save results

The output matrices are saved in text files with values rounded to 3 decimal places, and detailed verification results are printed to the console.

## 🧪 Environment

This code is implemented and tested in **Google Colab** using standard Python libraries.

## 🚀 How to Run

1. Open the notebook or script in **Google Colab** or your local Python environment.
2. Upload or prepare the matrix file named `matrix_a.txt` **or any other filename**. If you use a custom name, make sure to change the filename in the `main()` function inside the code block:
    ```python
    def main():
        try:
            A = read_matrix('your_matrix_file.txt')  # Change filename here
        except FileNotFoundError:
            print("Error: matrix_x.txt not found.")
            return
    ```

   Example format for the matrix file (e.g., `matrix_a.txt`):
    ```
    3 3
    2 -1 0
    -1 2 -1
    0 -1 2
    ```
    
4. Run the script or call the `main()` function.
5. The output files `Q.txt`, `R.txt`(with every run the files will update) will be generated in the working directory also the result will apper on the console of the colab.


## ✅ Verification Steps

The script performs the following checks after decomposition:
- `A ≈ QR`: verifies matrix reconstruction
- `QᵀQ ≈ I`: checks orthogonality of Q
- Confirms that R is upper triangular

## 💻 Dependencies

- Python 3.6+
- numpy
- math

## ✅ Implementation Notes

- Uses only basic operations (no numpy.linalg functions)
- Handles both square and rectangular matrices
- Includes comprehensive verification checks
- Outputs rounded matrices while maintaining precision for calculations

## ✅ Testing

The program has been tested with:

Square matrices (3×3)

Rectangular matrices (2×4)

Edge cases (zero elements, near-zero elements)
