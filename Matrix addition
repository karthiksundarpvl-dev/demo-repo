/**
 * Function to add two matrices
 * @param {number[][]} matrixA - First matrix
 * @param {number[][]} matrixB - Second matrix
 * @returns {number[][]} - Resultant matrix after addition
 */
function addMatrices(matrixA, matrixB) {
    // Validate that both inputs are arrays
    if (!Array.isArray(matrixA) || !Array.isArray(matrixB)) {
        throw new Error("Both inputs must be 2D arrays (matrices).");
    }

    // Validate dimensions
    const rowsA = matrixA.length;
    const rowsB = matrixB.length;
    if (rowsA !== rowsB) {
        throw new Error("Matrices must have the same number of rows.");
    }

    const colsA = matrixA[0].length;
    const colsB = matrixB[0].length;
    if (colsA !== colsB) {
        throw new Error("Matrices must have the same number of columns.");
    }

    // Validate all elements are numbers
    for (let i = 0; i < rowsA; i++) {
        if (!Array.isArray(matrixA[i]) || !Array.isArray(matrixB[i])) {
            throw new Error("Each row must be an array.");
        }
        if (matrixA[i].length !== colsA || matrixB[i].length !== colsB) {
            throw new Error("All rows must have the same number of columns.");
        }
        for (let j = 0; j < colsA; j++) {
            if (typeof matrixA[i][j] !== "number" || typeof matrixB[i][j] !== "number") {
                throw new Error("Matrix elements must be numbers.");
            }
        }
    }

    // Perform addition
    const result = [];
    for (let i = 0; i < rowsA; i++) {
        result[i] = [];
        for (let j = 0; j < colsA; j++) {
            result[i][j] = matrixA[i][j] + matrixB[i][j];
        }
    }

    return result;
}

// Example usage:
try {
    const matrix1 = [
        [1, 2, 3],
        [4, 5, 6]
    ];
    const matrix2 = [
        [7, 8, 9],
        [10, 11, 12]
    ];

    const sumMatrix = addMatrices(matrix1, matrix2);
    console.log("Matrix 1:", matrix1);
    console.log("Matrix 2:", matrix2);
    console.log("Sum Matrix:", sumMatrix);
} catch (error) {
    console.error("Error:", error.message);
}
