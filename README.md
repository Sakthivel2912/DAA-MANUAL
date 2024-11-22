# Design and Analysis of Algorithms Lab (CS23331)

This repository contains programs and solutions related to **Design and Analysis of Algorithms (DAA)**, focusing on **C programming basics**, time complexity analysis, and algorithmic strategies like divide-and-conquer, dynamic programming, and greedy approaches. The code samples were extracted and structured from lab exercises, including various problems and solutions.

## Table of Contents

1. **Basic C Programming Practice**
    - Swapping numbers
    - Eligibility checks
    - Discounts and conditions
    - Mathematical computations (factorial, Fibonacci, powers, etc.)
    - Prime and even/odd checks

2. **Time Complexity Analysis**
    - Counter method for complexity determination
    - Nested loop analysis
    - Algorithmic time complexities explained with programs

3. **Divide and Conquer**
    - Count zeroes in a sorted array
    - Majority element identification
    - Recursive algorithms for sums and searches
    - Quick sort implementation

4. **Greedy Algorithms**
    - Coin change problem
    - Maximum array sum with greedy optimization
    - Rearranging arrays for minimum sum products

5. **Dynamic Programming**
    - Chessboard path maximization
    - Longest common subsequence
    - Longest non-decreasing subsequence

6. **Array Operations**
    - Finding duplicates
    - Intersection of sorted arrays
    - Pairing with given differences

## How to Use

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-repo-name/DAA-Lab.git
Navigate to the Directory
bash
Copy code
cd DAA-Lab
Compile the Programs Use any C compiler to compile the .c files. For example:
bash
Copy code
gcc program_name.c -o program_name
./program_name
Examples
Example: Fibonacci Series Calculation
c
Copy code
#include<stdio.h>
int main(){
    int n, a = 0, b = 1, c;
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        c = a + b;
        a = b;
        b = c;
    }
    printf("%d", a);
    return 0;
}
Example: Quick Sort Implementation
c
Copy code
#include <stdio.h>
void quickSort(int[], int, int);
int partition(int[], int, int);
int main() {
    int arr[100], n;
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    quickSort(arr, 0, n-1);
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}
void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high);
        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}
int partition(int arr[], int low, int high) {
    int pivot = arr[high];
    int i = (low - 1);
    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }
    int temp = arr[i + 1];
    arr[i + 1] = arr[high];
    arr[high] = temp;
    return (i + 1);
}
Author
Vignesh R
Student ID: 2116231801508
Rajalakshmi Engineering College
