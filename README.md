# EX-21-POINTERS
# AIM:
Write a c program to add two integer numbers using pointers.

## ALGORITHM:
```
1.Start the program and declare three integers: num1, num2, and sum.
2.Read two integer inputs from the user into num1 and num2.
3.Create pointers pointing to num1, num2, and sum.
4.Use the pointers to add the values of num1 and num2, and store the result in sum.
5.Print the result using the pointer values and end the program.
```

## PROGRAM:
```
#include <stdio.h>
int main()
{
  int num1,num2,sum=0.0;
  
  scanf("%d %d",&num1,&num2);
  int *pnum1=&num1,*pnum2=&num2,*psum=&sum;
  *psum=*pnum1 + *pnum2;
  printf("%d + %d = %d",*pnum1,*pnum2,*psum);
  return 0;
}
```

## OUTPUT:
 	
![image](https://github.com/user-attachments/assets/fc15a878-3440-4037-8c63-c6149074ad00)



## RESULT:
Thus the program to add two integer numbers using pointers has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:
```
1.Start and declare a function prd(int *x) to calculate the product recursively.
2.In main(), initialize x = 1 and pass its address to the prd function.
3.In prd(), return 1 if *x == 13 (base case).
4.Otherwise, multiply *x with the result of prd() called on the next number (*x + 1).
5.Print the final product result in main() and end the program.
```

## PROGRAM:
```
#include<stdio.h>
int prd(int *x)
{
    int pro=1;
  if(*x==13){
      return 1;
  }
    int n=*x+1;
    return pro=*x*prd(&n);
    
}
int main()
{
    int x=1;
    int(*prdf)(int*)=prd;
    printf("Product is = %d",prdf(&x));
    return 0;
    
}
```

## OUTPUT:


![image](https://github.com/user-attachments/assets/a30ae70b-98e0-4c43-90c4-bc0e46e7513d)


         		
## RESULT:

Thus the program to calculate the Product of first 12 natural numbers using Recursion has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row and column of a Matrix

## ALGORITHM:
```
1.Start the program and read matrix dimensions x (rows) and y (columns).

2.Input elements into a 2D array a[x][y].

3.Loop through each row to calculate and print the sum of its elements.

4.Loop through each column to calculate and print the sum of its elements.

4.End the program.

```
## PROGRAM:

```
#include <stdio.h>

int main()
{
    int x,y,i,j;
    scanf("%d %d",&x,&y);
    int a[x][y];
    for(i=0;i<x;i++)
    {
        for(j=0;j<y;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    for(i=0;i<x;i++)
    {
        int sum=0;
        for(j=0;j<y;j++)
        {
            sum+=a[i][j];
        }
        printf("The Sum of Elements of a Row in a Matrix:  %d\n",sum);
    }
    for(j=0;j<y;j++)
    {
        int sum1=0;
        for(i=0;i<x;i++)
        {
            sum1+=a[i][j];
        }
        printf("The Sum of Elements of a Column in a Matrix:  %d\n",sum1);
    }
    return 0;
}
```


## OUTPUT

![Screenshot 2025-05-22 091541](https://github.com/user-attachments/assets/8067cb2e-fbb3-4423-afdf-9e470eb68a63)



 ## RESULT
 
Thus the program to  find Sum of each row and column of a Matrix has been executed successfully.
 

# EX-24-STRINGS

## AIM:

Write a program in C to find the number of times a given word 'the' appears in the given string.

## ALGORITHM:

```
Start the program and read a line of text into str.

Use strtok() to split the string into words using space and newline as delimiters.

Initialize a counter count to 0.

For each word, compare it with "the" using strcmp(). If it matches, increment count.

Print the frequency and end the program.

```


## PROGRAM:
```
#include <stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int count=0;
    fgets(str,sizeof(str),stdin);
    char *token=strtok(str," \n");
    while(token!=NULL){
        if(strcmp(token,"the")==0){
            count++;
        }
        token=strtok(NULL," \n");
    }
    printf("The frequency of the word 'the' is : %d",count);
    return 0;
  
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/700792d8-f538-4ae6-8b01-20e10940811f)

![Screenshot 2025-05-22 092301](https://github.com/user-attachments/assets/d436364a-9084-4bc3-8ed7-61cc8821acda)

## RESULT

Thus the C program to find the number of times a given word 'the' appears in the given string has been executed successfully.
 
## EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 3 integer elements using pointer

## ALGORITHM
```
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[n] to hold up to n elements.
•	Integer pointer ptr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address ptr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(ptr + i) using pointer dereferencing.
Step 6: End the program.
```

## PROGRAM
```
#include <stdio.h>

int main() {
    int n;
    scanf("%d",&n);
    int arr[n];
    int *ptr = arr
   
    for (int i = 0; i < n; i++) {
        scanf("%d", ptr + i);
    }

   
    for (int i = 0; i < n; i++) {
        printf("the elements are %d\n", *(ptr + i));
    }

    return 0;
}

```

## OUTPUT

![Screenshot 2025-05-22 093009](https://github.com/user-attachments/assets/e1213bf3-42d5-4c9b-b64e-09ac94070d1f)

 

## RESULT

Thus the C program to read and display an array of any 3 integer elements using pointer has been executed


