Count even and odd element in Java
Here, in this page we will discuss the program to count even and odd element in java programming language. We are given with an integer array and need to print the count of even and odd elements present in it.

Counting even and odd element in Java
Example
arr[] = [101, 200, 301, 400, 501]
Even Elements count = 2 (200, 400)
Odd Elements count = 3 (101, 301, 501)
Here, we will discuss the following two methods to print the count of even elements and odd elements.

Method 1 : Using Modulo operator
Method 2 : Using Bit-wise AND operator.
Let’s discuss above two methods one by one,

Method 1 :
Take two variables, countEven=0, countOdd=0.
Iterate over the array,
Increment countEven if(arr[i]%2==0)
Otherwise increment the value of countOdd by 1.
Modulo Operator
The modulo operator, denoted by %, is an arithmetic operator. The modulo division operator produces the remainder of an integer division. Syntax: If x and y are integers, then the expression: x % y. produces the remainder when x is divided by y.
So, if a number is even then it return 0 on modulo it by 2, otherwise it return 1
Method 1 : Code in Java
Run
class Main{
  public static void main (String[] args)
  {
     int arr[] = {1, 20, 60, 31, 75, 40, 80};
     int n = arr.length;
     int countEven = 0, countOdd = 0;

     for(int i=0; i<n; i++){
         if((arr[i] % 2 )== 0)
           countEven += 1;

         else
           countOdd += 1;
     }
     System.out.println("Even Elements count : "+ countEven);
     System.out.println("Odd Elements count : "+ countOdd);
  }
}
Output :
Even Elements count : 4
Odd Elements count : 3
Related Pages
Finding Minimum scalar product of two vectors

Finding Maximum scalar product of two vectors in an array

Find all Symmetric pairs in an array 

Find maximum product sub-array in a given array

Finding Arrays are disjoint or not

Method 2 :
In this method we will use bit-wise AND operator. By doing AND of 1 with array element, if the result comes out to be 0 then the number is even otherwise odd.

Bit-wise AND Operator
The bitwise AND operator ( & ) compares each bit of the first operand to the corresponding bit of the second operand. If both bits are 1, the corresponding result bit is set to 1.
Otherwise, the corresponding result bit is set to 0. Both operands to the bit-wise AND operator must have integral types.
Method 2 : Code in Java
Run
class Main{
  public static void main (String[] args)
  {
     int arr[] = {1, 20, 60, 31, 75, 40, 80};
     int n = arr.length;
     int countEven = 0, countOdd = 0;

     for(int i=0; i<n; i++){
         if((arr[i] & 1 )== 0)
           countEven += 1;

         else
           countOdd += 1;
     }
     System.out.println("Even Elements count : "+ countEven);
     System.out.println("Odd Elements count : "+ countOdd);
  }
}
Output :
Even Elements count : 4
Odd Elements count : 3
