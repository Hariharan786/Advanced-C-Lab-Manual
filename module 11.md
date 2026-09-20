

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```c
#include <stdio.h>

int max_of_four(int a, int b, int c, int d) {
    int max = a;
    if (b > max) max = b;
    if (c > max) max = c;
    if (d > max) max = d;
    return max;
}

int main() {
    int n1, n2, n3, n4;
    printf("Enter four integers: ");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);
    int greater = max_of_four(n1, n2, n3, n4);
    printf("Greatest number is: %d\n", greater);
    return 0;
}
```

Output:
```text
Enter four integers: 10 20 15 5
Greatest number is: 20
```

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```c
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;
    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            int current_a = i & j;
            int current_o = i | j;
            int current_x = i ^ j;
            
            if (current_a < k && current_a > a) a = current_a;
            if (current_o < k && current_o > o) o = current_o;
            if (current_x < k && current_x > x) x = current_x;
        }
    }
    printf("%d\n%d\n%d\n", a, o, x);
}

int main() {
    int n, k;
    printf("Enter n and k: ");
    scanf("%d %d", &n, &k);
    calculate_the_max(n, k);
    return 0;
}
```

Output:
```text
Enter n and k: 5 4
2
3
3
```

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int noshel, noque;
    printf("Enter number of shelves and queries: ");
    scanf("%d %d", &noshel, &noque);
    
    int **shelarr = (int **)malloc(noshel * sizeof(int *));
    int *nobookarr = (int *)calloc(noshel, sizeof(int));
    
    for (int i = 0; i < noshel; i++) {
        shelarr[i] = NULL;
    }
    
    printf("Enter queries (type shelf_id [book_id]):\n");
    for (int i = 0; i < noque; i++) {
        int type, x, y;
        scanf("%d", &type);
        if (type == 1) {
            scanf("%d %d", &x, &y);
            nobookarr[x]++;
            shelarr[x] = (int *)realloc(shelarr[x], nobookarr[x] * sizeof(int));
            shelarr[x][nobookarr[x] - 1] = y;
        } else if (type == 2) {
            scanf("%d %d", &x, &y);
            printf("Book: %d\n", shelarr[x][y]);
        } else if (type == 3) {
            scanf("%d", &x);
            printf("Number of books on shelf %d: %d\n", x, nobookarr[x]);
        }
    }
    
    for (int i = 0; i < noshel; i++) {
        free(shelarr[i]);
    }
    free(shelarr);
    free(nobookarr);
    
    return 0;
}
```

Output:
```text
Enter number of shelves and queries: 2 3
Enter queries (type shelf_id [book_id]):
1 0 15
1 0 20
2 0 1
Book: 20
```


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, sum = 0;
    printf("Enter number of integers: ");
    scanf("%d", &n);
    
    int *a = (int *)malloc(n * sizeof(int));
    printf("Enter %d integers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }
    
    printf("Sum is: %d\n", sum);
    free(a);
    return 0;
}
```

Output:
```text
Enter number of integers: 5
Enter 5 integers: 1 2 3 4 5
Sum is: 15
```

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```c
#include <stdio.h>
#include <ctype.h>

int main() {
    char sentence[256];
    int count = 0, isWord = 0;
    
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);
    
    for (int i = 0; sentence[i] != '\0'; i++) {
        if (!isspace(sentence[i])) {
            if (!isWord) {
                isWord = 1;
                count++;
            }
        } else {
            isWord = 0;
        }
    }
    
    printf("Total word count: %d\n", count);
    return 0;
}
```

Output:
```text
Enter a sentence: Hello world, this is C programming!
Total word count: 6
```



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
