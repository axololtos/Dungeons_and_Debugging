# Dungeons n Debugging: Home of Upside down Hackathon team
Dungeons &amp; Debugging: Masters of the Technologies from Upside Down
Certainly! Let us embark on a whimsical journey into the digital abyss, where lines of code intersect with the eerie echoes of the Upside Down. Behold, the tale of **Dungeons & Debugging: The Master of Technologies from the Upside Down**! 🚀🔮👾

---

## **The Chronicles of Dungeons & Debugging**

### **Chapter I: The Code Portal**

In the heart of Hacker's Hollow, where the flickering screens cast shadows on ancient cobwebs, lies the clandestine lair of **Dungeons & Debugging**. Their mission? To unravel the mysteries of the Upside Down—one line of code at a time.

#### **1. Sir Syntax, the Code Knight:**
Armed with a keyboard forged in the fires of binary, Sir Syntax leads the charge. His hoodie bears the emblem of a dragon entwined with curly braces. His battle cry? "Fear not, for I shall debug this tangled web and restore order to the realm of Softwaredom!"

#### **2. Lady Logic, the Debugger Sorceress:**
Her eyes glow with hexadecimal wisdom. Lady Logic weaves spells of conditional statements and truth tables. She can spot a logical fallacy from a mile away. "Fear not," she whispers, "we shall follow the breadcrumbs of reason and emerge victorious!"

### **Chapter II: The Cryptic Cryptocurrency**

Deep within the Upside Down, they encounter treacherous stack traces—the cryptic whispers of forgotten algorithms. Each line of error messages is a riddle waiting to be solved. "Fear not," declares Mage Memory, the Memory Alchemist. "We shall reclaim lost pointers and banish memory leaks!"

### **Chapter III: The Merge Conflict Dragon**

At the gates of deployment, they face the formidable Merge Conflict Dragon. Its scales are made of nitpicks, and its fiery breath smells suspiciously like linters. "Fear not," proclaims Sir Mergealot, the Git knight. "We shall resolve this conflict and merge our destinies!"

### **Chapter IV: The README Scrolls**

Scribe Syntaxia, the Documentation Mage, transcribes incantations into README scrolls. Her quill dances across parchment, ensuring that future generations understand the arcane codebase. "Fear not," she insists, "we shall annotate our code scrolls and appease the Code Review Dragon!"

And so, dear hackathon judges, behold **Dungeons & Debugging**: where wizards wield IDEs, dragons guard pull requests, and the binary moon shines bright. May their pull requests be swift, their tests pass, and their coffee always hot! 🌟☕✨

Remember, in the Upside Down of code, bugs are the true Demogorgons. Happy hacking, brave adventurers! 🚀🔍🌌




import java.util.Scanner;

public class MatrixOperations {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Initialize 2x2 Matrices
        int[][] matrixA = new int[2][2];
        int[][] matrixB = new int[2][2];

        System.out.println("Enter elements of 2x2 matrix A:");
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                matrixA[i][j] = scanner.nextInt();
            }
        }

        System.out.println("Enter elements of 2x2 matrix B:");
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                matrixB[i][j] = scanner.nextInt();
            }
        }

        scanner.close();

        // Perform Operations and Display Results
        int[][] resultAddition = addMatrices(matrixA, matrixB);
        int[][] resultSubtraction = subtractMatrices(matrixA, matrixB);
        int[][] resultMultiplication = multiplyMatrices(matrixA, matrixB);

        System.out.println("Matrix A + Matrix B:");
        printMatrix(resultAddition);

        System.out.println("Matrix A - Matrix B:");
        printMatrix(resultSubtraction);

        System.out.println("Matrix A * Matrix B:");
        printMatrix(resultMultiplication);
    }

    // Method for Matrix Addition
    public static int[][] addMatrices(int[][] a, int[][] b) {
        int rows = a.length;
        int cols = a[0].length;
        int[][] result = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[i][j] = a[i][j] + b[i][j];
            }
        }
        return result;
    }

    // Method for Matrix Subtraction
    public static int[][] subtractMatrices(int[][] a, int[][] b) {
        int rows = a.length;
        int cols = a[0].length;
        int[][] result = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[i][j] = a[i][j] - b[i][j];
            }
        }
        return result;
    }

    // Method for Matrix Multiplication
    public static int[][] multiplyMatrices(int[][] a, int[][] b) {
        int rowsA = a.length;
        int colsA = a[0].length;
        int colsB = b[0].length;
        int[][] result = new int[rowsA][colsB];

        for (int i = 0; i < rowsA; i++) {
            for (int j = 0; j < colsB; j++) {
                result[i][j] = 0;
                for (int k = 0; k < colsA; k++) {
                    result[i][j] += a[i][k] * b[k][j];
                }
            }
        }
        return result;
    }

    // Method to Print Matrix
    public static void printMatrix(int[][] matrix) {
        for (int[] row : matrix) {
            for (int element : row) {
                System.out.print(element + " ");
            }
            System.out.println();
        }
    }
}
