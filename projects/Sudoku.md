---
layout: project
type: project
image: img/Sodoku-Image.png
title: "Sodoku Solver"
date: 2023-10-23
labels:
  - Java
summary: "Java code that helps find an answer to a given Sodoku problem."
---
<img src=".../img/Sodoku-Image.png">

## About

This was a project that I created that helps solve given Sodoku problems. In this project I used various algorithms to help solve any Sodoku problem and checks to see if it is valid. The program is designed to solve the given problem and return the problem and solution. 

## Reflection

In this project I used various parameters and minor recursion to fullfill its duty. First I used a wide array of if statements in order to find if the problem is valid. I also used recursion to find the solution to the problem by calling itself and checking to see a valid input. 

In this project my knowledge of Java greatly increased as it improved my insight to how recursion works and uses various Java syntax that will deem useful in future projects. 

## Main Code

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sudoku Java Code</title>
    
    <!-- Highlight.js for Syntax Highlighting -->
    <link rel="stylesheet" 
          href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/styles/default.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/highlight.min.js"></script>
    <script>hljs.highlightAll();</script>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 20px;
            padding: 20px;
        }
        pre {
            background-color: #2d2d2d;
            color: #ffffff;
            padding: 15px;
            border-radius: 5px;
            overflow-x: auto;
            font-size: 14px;
        }
        h2 {
            color: #333;
        }
    </style>
</head>
<body>
    <h2>Sudoku Solver Java Code</h2>
    <pre><code class="language-java">
public class Sudoku {

    /* check that the sudoku rules hold in this sudoku puzzle.
     * cells that contain 0 are not checked.
     * @param the sudoku to be checked
     * @param whether to print the error found, if any
     * @return true if this sudoku obeys all of the sudoku rules, otherwise false
     */
    
    public static boolean checkSudoku(int[][] sudoku, boolean printErrors) { 
        if (sudoku.length != 9) { 
            if (printErrors) {
                System.out.println("sudoku has " + sudoku.length +
                                    " rows, should have 9");
            }
            return false;
        }
        for (int i = 0; i < sudoku.length; i++) {
            if (sudoku[i].length != 9) {
                if (printErrors) {
                    System.out.println("sudoku row " + i + " has " +
                                        sudoku[i].length + " cells, should have 9");
                }
                return false;
            }
        }
        /* check each cell for conflicts */
        for (int i = 0; i < sudoku.length; i++) {
            for (int j = 0; j < sudoku.length; j++) {
                int cell = sudoku[i][j];
                if (cell == 0) { 
                    continue;
                }
                if ((cell < 1) || (cell > 9)) {
                    if (printErrors) {
                        System.out.println("sudoku row " + i + " column " + j +
                                            " has illegal value " + cell);
                    }
                    return false;
                }
                /* check row */
                for (int m = 0; m < sudoku.length; m++) {
                    if ((j != m) && (cell == sudoku[i][m])) {
                        if (printErrors) {
                            System.out.println("sudoku row " + i + " has " + cell +
                                                " at both positions " + j + " and " + m);
                        }
                        return false;
                    }
                }
                /* check column */
                for (int k = 0; k < sudoku.length; k++) {
                    if ((i != k) && (cell == sudoku[k][j])) {
                        if (printErrors) {
                            System.out.println("sudoku column " + j + " has " + cell +
                                                " at both positions " + i + " and " + k);
                        }
                        return false;
                    }
                }
                /* check 3x3 grid */
                for (int k = 0; k < 3; k++) {
                    for (int m = 0; m < 3; m++) {
                        int testRow = (i / 3 * 3) + k;
                        int testCol = (j / 3 * 3) + m;
                        if ((i != testRow) && (j != testCol) &&
                            (cell == sudoku[testRow][testCol])) {
                            if (printErrors) {
                                System.out.println("sudoku character " + cell + " at row " +
                                                    i + ", column " + j + 
                                                    " matches character at row " + testRow +
                                                    ", column " + testCol);
                            }
                            return false;
                        }
                    }
                }
            }
        }
        return true;
    }

    /* convert sudoku to string */
    public static String toString(int[][] sudoku, boolean debug) {
        if ((!debug) || (checkSudoku(sudoku, true))) {
            String result = "";
            for (int i = 0; i < sudoku.length; i++) {
                if (i % 3 == 0) {
                    result += "+-------+-------+-------+\n";
                }
                for (int j = 0; j < sudoku.length; j++) {
                    if (j % 3 == 0) {
                        result += "| ";
                    }
                    if (sudoku[i][j] == 0) {
                        result += "  ";
                    } else {
                        result += sudoku[i][j] + " ";
                    }
                }
                result += "|\n";
            }
            result += "+-------+-------+-------+\n";
            return result;
        }
        return "illegal sudoku";
    }

    /* fill sudoku with solution */
    public static boolean fillSudoku(int[][] sudoku) {
        boolean allFilled = true;
        int row = -1; 
        int col = -1;
        
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                if (sudoku[i][j] == 0) {
                    row = i;
                    col = j;
                    allFilled = false;
                    break;
                }
            }
            if (!allFilled) {
                break;
            }
        }
        if (allFilled) {
            return true;
        }
        for (int num = 1; num <= 9; num++) {
            sudoku[row][col] = num;
            if (checkSudoku(sudoku, false)) {
                if (fillSudoku(sudoku)) {
                    return true;
                }
            }
        }
        sudoku[row][col] = 0;
        return false;
    }
}
    </code></pre>
</body>

## Test Code

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sudoku Solver - Java Code</title>
    
    <!-- Highlight.js for Syntax Highlighting -->
    <link rel="stylesheet" 
          href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/styles/default.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/highlight.min.js"></script>
    <script>hljs.highlightAll();</script>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 20px;
            padding: 20px;
        }
        pre {
            background-color: #2d2d2d;
            color: #ffffff;
            padding: 15px;
            border-radius: 5px;
            overflow-x: auto;
            font-size: 14px;
        }
        h2 {
            color: #333;
        }
    </style>
</head>
<body>
    <h2>SudokuTest Java Code</h2>
    <pre><code class="language-java">
package hw11;
/* 
 * test a Sudoku solver
 * @author  Biagioni, Edoardo
 * @date    October 23, 2013
 * @bugs    none
 */
public class SudokuTest {

    private static boolean isFilled(int[][] sudoku) {
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                if (sudoku[i][j] == 0) {
                    return false;
                }
            }
        }
        return true;
    }

    private static int[][] sameSudoku(int[][] sudoku, int[][] solution) {
        int[][] result = new int[9][9];
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                result[i][j] = sudoku[i][j];
            }
        }
        boolean same = true;
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                if (result[i][j] != solution[i][j]) {
                    same = false;
                    result[i][j] = 0;
                }
            }
        }
        return same ? null : result;
    }

    private static void testSudoku(String name, int[][] sudoku, int[][] solution) {
        System.out.println("Solving " + name + "\n" + Sudoku.toString(sudoku, true));
        if (Sudoku.fillSudoku(sudoku)) {
            if (isFilled(sudoku) && Sudoku.checkSudoku(sudoku, true)) {
                System.out.println("Success!\n" + Sudoku.toString(sudoku, true));
                if (solution != null) {
                    int[][] diff = sameSudoku(sudoku, solution);
                    if (diff != null) {
                        System.out.println("Given solution:\n" + Sudoku.toString(solution, true));
                        System.out.println("Difference between solutions:\n" + Sudoku.toString(diff, true));
                    }
                }
            } else {
                if (!isFilled(sudoku)) {
                    System.out.println("Sudoku was not completely filled:\n" + Sudoku.toString(sudoku, false));
                }
                if (!Sudoku.checkSudoku(sudoku, false)) {
                    System.out.println("Sudoku is not a valid solution:\n" + Sudoku.toString(sudoku, false));
                }
            }
        } else {
            System.out.println("Unable to complete sudoku " + name + "\n" + Sudoku.toString(sudoku, true));
        }
    }

    public static void main(String[] args) {
        int[][] example1 = {
            {7, 8, 0, 0, 9, 0, 0, 2, 0},
            {1, 0, 0, 0, 0, 0, 9, 6, 4},
            {0, 0, 0, 2, 5, 1, 0, 0, 0},
            {0, 0, 6, 1, 8, 5, 0, 0, 0},
            {5, 0, 4, 0, 0, 0, 3, 0, 2},
            {0, 0, 0, 3, 4, 2, 5, 0, 0},
            {0, 0, 0, 9, 6, 3, 0, 0, 0},
            {6, 4, 1, 0, 0, 0, 0, 0, 3},
            {0, 9, 0, 0, 1, 0, 0, 5, 7}
        };

        int[][] solution1 = {
            {7, 8, 3, 4, 9, 6, 1, 2, 5},
            {1, 2, 5, 7, 3, 8, 9, 6, 4},
            {4, 6, 9, 2, 5, 1, 7, 3, 8},
            {2, 3, 6, 1, 8, 5, 4, 7, 9},
            {5, 1, 4, 6, 7, 9, 3, 8, 2},
            {9, 7, 8, 3, 4, 2, 5, 1, 6},
            {8, 5, 7, 9, 6, 3, 2, 4, 1},
            {6, 4, 1, 5, 2, 7, 8, 9, 3},
            {3, 9, 2, 8, 1, 4, 6, 5, 7}
        };

        testSudoku("Example 1", example1, solution1);
    }
}
    </code></pre>
</body>
