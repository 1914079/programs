






----
# **GURU NANAK DEV ENGINEERING COLLEGE, LUDHIANA.**
----
![LOGO](https://blog.coachingkaro.org/wp-content/uploads/2019/07/logo.jpg)
# **PROGRAMMING FOR PROBLEM SOLVING ESC-18105**
----
## **NAME** - ***NIKHIL***
## **ROLL NO.** - *1914079*
## **BRANCH** - *CIVIL ENGINEERING*
---
----

# PROGRAMS
```C
    Practical 1:  Write a C Program to Add Two Integers.
    Practical 2:  Write a C Program to Multiply two Floating .
    Practical 3:  Write a C Program to Check Whether a Number is Even or Odd using if else statement.
    Practical 4:  Write a C Program to calculate the sum of first 10 natural numbers using for loop.
    Practical 5:  Write a C Program to print EVEN numbers from 1 to N using while loop.
    Practical 6:  Write a C Program to print ODD numbers from 1 to N using do while loop.
    Practical 7:  Write a C Program to create a simple calculator using switch Statement.
    Practical 8:  Write a C Program to find the max between two numbers uding function.
    Practical 9:  Write a program in C to check whether a number is a prime or not using the function.
    Practical 10: Write a C Program for function (using call by value).
    Practical 11: Write a C Program for function (using call by reference).
    Practical 12: Write a C Program to take 5 values from the user and store them in an array. Print the
                  elements stored in the array.
    Practical 13: Write a C Program to find the average of n numbers using arrays.
    Practical 14: Write a C Program to accept Sorted Array and do Search using Binary Search .
    Practical 15: Write a C Program to Implement Linear Search.
    Practical 16: Write a C Program to Sort N Numbers in Ascending Order using Bubble Sort.
    Practical 17: Write a C program to declare, assign and access a pointer variable.
    Practical 18: Write a C Program to Store Information of a Student Using Structure
    Practical 19: Write a C Program to Find Factorial of a Number Using Recursion.
    Practical 20: Write a C Program to display Fibonacci Series using
```

----
## PRACTICAL 1. Write a C Program to Add Two Integers.
```C
#include<stdio.h>
void main()
{
        int a,b;
        printf("Enter the two number to be added\n");
        scanf("%d%d",&a,&b);
        printf("Sum  : %d + %d = %d \n",a,b,a+b);

}
```
### OUTPUT
```C
    Enter the two number to be added
    4
    5
    Sum  : 4 + 5 = 9 
```

----
## PRACTICAL 2. Write a C Program to Multiply two Floating Point Numbers
```C
#include <stdio.h>
int main()
{
    double firstNumber, secondNumber, product;
    printf("Enter two numbers: ");
    scanf("%lf %lf", &firstNumber, &secondNumber);  
    product = firstNumber * secondNumber;  
    printf("Product = %.2lf", product);
    
    return 0;
}
```

### OUTPUT
```C
    Enter two numbers: 1.2
    2.3
    Product = 2.76


```

----
## PRACTICAL 3. Write a C Program to Check Whether a Number is Even or Odd using if else statement
```C
#include <stdio.h>
int main()
{
    int number;
    printf("Enter an integer: ");
    scanf("%d", &number);
    if(number % 2 == 0)
        printf("%d is even.", number);
    else
        printf("%d is odd.", number);
    return 0;
}
```

### OUTPUT
```C
    Enter an integer: 5
    5 is odd.
```

----
## PRACTICAL 4. Write a C Program to calculate the sum of first 10 natural numbers using for loop.
```C
#include <stdio.h>
void main()
{
    int  j, sum = 0;
    printf("The first 10 natural number is :\n");
    for (j = 1; j <= 10; j++)
    {
        sum = sum + j;
        printf("%d ",j);    
    }
    printf("\nThe Sum is : %d\n", sum);
}
```

### OUTPUT
```C
    The first 10 natural number is :                                                                              
    1 2 3 4 5 6 7 8 9 10                                                                                          
    The Sum is : 55
```

----
## PRACTICAL 5. Write a C Program to print EVEN numbers from 1 to N using while loop.
```C
#include <stdio.h>
int main()
{
    int i, n;
    printf("Print all even numbers till: ");
    scanf("%d", &n);
    printf("All even numbers from 1 to %d are: \n", n);
    i=1;
    while(i<=n)
    {
        if(i%2==0)
        {
            printf("%d\n", i);
        }
        i++;
    }
    return 0;
}
```

### OUTPUT
```C
    Print all even numbers till: 7
    All even numbers from 1 to 7 are: 
    2
    4
    6
```

----
## PRACTICAL 6. Write a C Program to print ODD numbers from 1 to N using do while loop.
```C
#include<stdio.h>
int main()
{
	int number;
	int n;
	number=1;
	printf("Enter the value of N: ");
	scanf("%d",&n);
	printf("Odd Numbers from 1 to %d:\n",n);
	while(number<=n)
	{
		if(number%2 != 0)
			printf("%d ",number);
				number++;
	}
	return 0;
}
```

### OUTPUT
```C
    Enter the value of N: 7
    Odd Numbers from 1 to 7:
    1 3 5 7 
```

----
## PRACTICAL 7. Write a C Program to create a simple calculator using switch Statement.
```C
#include<stdio.h>
int main() 
{
    char operator;
    double firstNumber,secondNumber;
    printf("Enter an operator (+, -, *,): ");
    scanf("%c", &operator);
    printf("Enter two operands: ");
    scanf("%lf %lf",&firstNumber, &secondNumber);
    switch(operator)
    {
        case '+':
            printf("%.1lf + %.1lf = %.1lf",firstNumber, secondNumber, firstNumber + secondNumber);
            break;
        case '-':
            printf("%.1lf - %.1lf = %.1lf",firstNumber, secondNumber, firstNumber - secondNumber);
            break;
        case '*':
            printf("%.1lf * %.1lf = %.1lf",firstNumber, secondNumber, firstNumber * secondNumber);
            break;
        case '/':
            printf("%.1lf / %.1lf = %.1lf",firstNumber, secondNumber, firstNumber / secondNumber);
            break;
        // operator doesn't match any case constant (+, -, *, /)
        default:
            printf("Error! operator is not correct");
    }
    
    return 0;
}
```

### OUTPUT
```C
    Enter an operator (+, -, *,): +
    Enter two operands: 45
    8
   45.0 + 8.0 = 53.0
```
----
## PRACTICAL 8. Write a C Program to find the max between two numbers uding function 
```C
#include <stdio.h>
int max(int num1, int num2);
int main() 
{
    int num1, num2, maximum;
    printf("Enter any two numbers: ");
    scanf("%d%d", &num1, &num2);
    maximum = max(num1, num2); 
    printf("\nMaximum = %d\n", maximum);
    return 0;
}
int max(int num1, int num2)
{
    return (num1 > num2 ) ? num1 : num2;
}
```

### OUTPUT
```C
    Enter any two numbers: 45
    67

    Maximum = 67
```

## PRACTICAL 9. Write a program in C to check whether a number is a prime or not using the function.
```C
#include<stdio.h>
int check_prime(int);
main()
{
   int n, result;
   printf("Enter an integer to check whether it is prime or not.\n");
   scanf("%d",&n);
   result = check_prime(n);
   if ( result == 1 )
      printf("%d is prime.\n", n);
   else
      printf("%d is not prime.\n", n);
   return 0;
}
int check_prime(int a)
{
   int c;
   for ( c = 2 ; c <= a - 1 ; c++ )
   { 
      if ( a%c == 0 )
     return 0;
   }
   return 1;
}
```

### OUTPUT
```C
    Enter an integer to check whether it is prime or not.
    11
    11 is prime.
```
----
## PRACTICAL 10. Write a C Program for function (using call by value)
```C
#include<stdio.h>
void swap(int a,int b);
void main()
{
int x,y;
printf("\n Enter value for x:");
scanf("%d",&x);
printf("\n Enter value for y:");
scanf("%d",&y);
printf("\n Before calling swap function\n");
printf("\n Value of x=%d,Value of y=%d\n",x,y);
swap(x,y);
printf("\n After returning from swap function");
printf("\n Value of x=%d,value of y=%d\n",x,y);
}
void swap(int a,int b)
{
int temp;
printf("\n Inside the function \n");
printf("\n Value of a=%d,Value of b=%d before swaping\n",a,b);
temp=a;
a=b;
b=temp;
printf("\n Value of a=%d,Value of b=%d after swaping\n",a,b);
}
```

### OUTPUT
```C

    Enter value for x:65
    Enter value for y:89

    Before calling swap function
    Value of x=65,Value of y=89

    Inside the function 

    Value of a=65,Value of b=89 before swaping
    Value of a=89,Value of b=65 after swaping

    After returning from swap function
    Value of x=65,value of y=89
```
----
## PRACTICAL 11. Write a C Program for function (using call by reference).
```C
#include<stdio.h>
void swap(int *,int *);
void main()
{
int x,y;
printf("\n Enter value for x:");
scanf("%d",&x);
printf("\n Enter value for y:");
scanf("%d",&y);
printf("\n Before calling swap function\n");
printf("\n Value of x=%d,Value of y=%d\n",x,y);
swap(&x,&y);
printf("\n After returning from swap function");
printf("\n Value of x=%d,value of y=%d\n",x,y);
}
void swap(int *a,int *b)
{
int temp;
printf("\n Inside the function \n");
printf("\n Value of a=%d,Value of b=%d before swaping\n",*a,*b);
temp=*a;
*a=*b;
*b=temp;
printf("\n Value of a=%d,Value of b=%d after swaping\n",*a,*b);
}
```

### OUTPUT
```C
    Enter value for x:56
    Enter value for y:78

    Before calling swap function
    Value of x=56,Value of y=78

    Inside the function 

    Value of a=56,Value of b=78 before swaping
    Value of a=78,Value of b=56 after swaping

    After returning from swap function
    Value of x=78,value of y=56
```

----
## PRACTICAL 12. Write a C Program to take 5 values from the user and store them in an array. Print the elements stored in the array
```C
#include <stdio.h>
int main() 
{
  int values[5];
  printf("Enter 5 integers: ");
  for(int i = 0; i < 5; ++i) {
     scanf("%d", &values[i]);
  }
  printf("Displaying integers: ");
  for(int i = 0; i < 5; ++i)
  {
     printf("%d\n", values[i]);
  }
  return 0;
}
```

### OUTPUT
```C
    Enter 5 integers: 52
    12
    36
    91
    03
    Displaying integers: 52
    12
    36
    91
    3
```

----
## PRACTICAL 13. Write a C Program to find the average of n numbers using arrays.
```C
#include <stdio.h>
int main()
{
    int n, i;
    float num[100], sum = 0.0, average;
    printf("Enter the numbers of elements: ");
    scanf("%d", &n);
    while (n > 100 || n <= 0)
    {
        printf("Error! number should in range of (1 to 100).\n");
        printf("Enter the number again: ");
        scanf("%d", &n);
    }
    for(i = 0; i < n; ++i)
    {
        printf("%d. Enter number: ", i+1);
        scanf("%f", &num[i]);
        sum += num[i];
    }
    average = sum / n;
    printf("Average = %.2f", average);
    return 0;
}
```

### OUTPUT
```C
    Enter the numbers of elements: 5
    1. Enter number: 78
    2. Enter number: 98
    3. Enter number: 32
    4. Enter number: 08
    5. Enter number: 72
    Average = 57.60
```
----
## PRACTICAL 14. Write a C Program to accept Sorted Array and do Search using Binary Search .
```C
#include<stdio.h>
int main()      
{               
        int m,n,a[100],search,first,last,middle;
        printf("Enter the size of array");
        scanf("%d",&m);
                
        printf("Enter %d numbar\n",m);
                
        for(n=0;n<m;n++)
                scanf("%d",&a[n]);
        printf("Enter the the number u want to search\n");
        scanf("%d",&search);

        first=0;
        last=m-1;
        middle=(first+last)/2;

        while(first<=last)
        {
                if(a[middle]<search)
                        first=middle+1;
                else if(a[middle]==search)
                {
                        printf("%d found at location %d\n",search,middle+1);
                        break;
                }
                else
                        last=middle-1;
                middle=(first+last)/2;
        }
        if(first>last)
                printf("Not found! %d is not present in the list \n",search);
        return 0;
}
```

### OUTPUT
```C
    Enter the size of array6
    Enter 6 numbar
    75
    33
    42
    12
    76
    22
    Enter the the number u want to search
    42
    42 found at location 3
```
----
## PRACTICAL 15. Write a C Program to Implement Linear Search
```C
#include <stdio.h>
int main()
{
  int array[100], search, c, n;
  printf("Enter number of elements in array\n");
  scanf("%d", &n);
  printf("Enter %d integer(s)\n", n);
  for (c = 0; c < n; c++)
    scanf("%d", &array[c]);
  printf("Enter a number to search\n");
  scanf("%d", &search);
  for (c = 0; c < n; c++)
  {
    if (array[c] == search)    /* If required element is found */
    {
      printf("%d is present at location %d.\n", search, c+1);
      break;
    }
  }
  if (c == n)
    printf("%d isn't present in the array.\n", search);
return 0;
}
```

### OUTPUT
```C
    Enter number of elements in array
    6
    Enter 6 integer(s)
    45
    63
    12
    23
    89
    77
    Enter a number to search
    23
    23 is present at location 4.
```
 ----
 ## PRACTICAL 16. Write a C Program to Sort N Numbers in Ascending Order using Bubble Sort.
 ```C
#include<stdio.h>
int main()
{
        int i,n,k,temp;
        printf("\n enter the array size\n");
        scanf("%d",&n);
        int a[n];
        printf("enter %d elements of array\n",n);
        for(i=0;i<n;i++)
                scanf("%d",&a[i]);
        for(k=0;k<n-1;k++)
        {
                for(i=0;i<n-k-1;i++)
                {
                        if(a[i]>a[i+1])
                        {
                                temp=a[i];
                                a[i]=a[i+1];
                                a[i+1]=temp;
                        }
                }
        }
        printf("\n array elements after shorting\n");
        for(i=0;i<n;i++)
                printf("%d\t",a[i]);
        printf("\n");
}
```

### OUTPUT
```C
    enter the array size
    6
    enter 6 elements of array
    32
    56
    78
    105
    90
    23

    array elements after shorting
    23   32   56   78   90   105	
```

----
## PRACTICAL 17. Write a C program to declare, assign and access a pointer variable.
```C
#include <stdio.h>

int main()
{
    int num;    /*declaration of integer variable*/
    int *pNum;  /*declaration of integer pointer*/
 
    pNum=& num; /*assigning address of num*/
    num=100;    /*assigning 100 to variable num*/
 
    //access value and address using variable num
    printf("Using variable num:\n");
    printf("value of num: %d\naddress of num: %u\n",num,&num);
    //access value and address using pointer variable num
    printf("Using pointer variable:\n");
    printf("value of num: %d\naddress of num: %u\n",*pNum,pNum);
 
   return 0;
}
```
### OUTPUT
```C
    Using variable num:
    value of num: 100
    address of num: 2764564284
    Using pointer variable:
    value of num: 100
    address of num: 2764564284
```     
----
##  PRACTICAL 18. Write a C Program to Store Information of a Student Using Structure
```C
#include <stdio.h>
struct student
{
    char name[50];
    int roll;
    float marks;
} s[10];
int main()
{
    int i;
    printf("Enter information of students:\n");
    // storing information
    for(i=0; i<10; ++i)
    {
        s[i].roll = i+1;
        printf("\nFor roll number%d,\n",s[i].roll);
        printf("Enter name: ");
        scanf("%s",s[i].name);
        printf("Enter marks: ");
        scanf("%f",&s[i].marks);
        printf("\n");
    }
    printf("Displaying Information:\n\n");
    // displaying information
    for(i=0; i<10; ++i)
    {
        printf("\nRoll number: %d\n",i+1);
        printf("Name: ");
        puts(s[i].name);
        printf("Marks: %.1f",s[i].marks);
        printf("\n");
    }
    return 0;
}
```

### OUTPUT
```C   
    Enter information of students: 

    For roll number1,
    Enter name: Tom
    Enter marks: 98

    For roll number2,
    Enter name: Jerry
    Enter marks: 89
    .
    .
    .
    Displaying Information:

    Roll number: 1
    Name: Tom
    Marks: 98
    .
    .
    .
```

----
## PRACTICAL 19. Write a C Program to Find Factorial of a Number Using Recursion.
```C
#include <stdio.h>
long int multiplyNumbers(int n);
int main()
{
    int n;
    printf("Enter a positive integer: ");
    scanf("%d", &n);
    printf("Factorial of %d = %ld", n, multiplyNumbers(n));
    return 0;
}
long int multiplyNumbers(int n)
{
    if (n >= 1)
        return n*multiplyNumbers(n-1);
    else
        return 1;
}     
```
### OUTPUT
```C  
  Enter a positive integer: 6
  Factorial of 6 = 720
```

----
## PRACTICAL 20. Write a C Program to display Fibonacci Series using recursion,
```C
#include<stdio.h>
int Fibonacci(int);
int main()
{
   int n, i = 0, c;
   scanf("%d",&n);
   printf("Fibonacci series\n");
   for ( c = 1 ; c <= n ; c++ )
   {
      printf("%d\n", Fibonacci(i));
      i++; 
   }
   return 0;
}
int Fibonacci(int n)
{
   if ( n == 0 )
      return 0;
   else if ( n == 1 )
      return 1;
   else
      return ( Fibonacci(n-1) + Fibonacci(n-2) );
}
```
### OUTPUT
```C
    5
    Fibonacci series
    0
    1
    1
    2
    3
```

----
