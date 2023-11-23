# Calculate-the-sum-of-elements-in-an-array-in-CPP

Program to calculate the sum of elements in an array in C++
Here, in this page we will discuss a C++ Program to find the sum of the elements of an array in C++  programming language we are given with an array and need to print the sum of elements of the given input array.

 

C code
While loop in C
Here, in this page we will discuss the following methods to find the sum of the elements of the given  input array.

Method 1 : Using Iteration
Method 2 : Top-down recursive approach
Method 3 : Bottom-up recursive approach.
 
Method 1 :
Declare a variable sum and initialize it to 0 i.e, sum=0
Run a loop from 0 to n,
Set sum = sum + arr[i]
After complete iteration print sum.
Method 1 : C++ Code
Run
#include<bits/stdc++.h>
using namespace std;

int main(){

   int arr[] = {10, 20, 30, 50, 89};

   int n = sizeof(arr)/sizeof(arr[0]); 

   int sum =0;

   for(int i=0; i<n; i++){
      sum += arr[i];
   }

   cout<<sum;
}
Output :
199
Related Pages
Find the Smallest and largest element in an array

Find Second Smallest Element in an Array

Reverse an Array

Sort first half in ascending order and second half in descending 

Sort the elements of an array

Method 2 :
Create a recursive function say getSum(int arr[], int index, int len)
If(index==len-1) return arr[index]
Otherwise, return (arr[index] + getSum(arr, index+1, len))
Method 2 : C++ Code
Run
#include<bits/stdc++.h>
using namespace std;

//Recursive Function
int getSum(int arr[], int index, int len){

     if(index==len-1)
      return arr[index];

     return arr[index] + getSum(arr, index+1, len);
}
int main(){

   int arr[] = {10, 20, 30, 50, 89};

   int n = sizeof(arr)/sizeof(arr[0]); 

   cout<<getSum(arr, 0, n);
}
Output :
199
While loop in C
Method 3 :
Create a recursive function say getSum(int arr[], int index)
If(index==0) return arr[index]
Otherwise, return (arr[index] + getSum(arr, index-1))
Method 3 : C++ Code
Run
#include<bits/stdc++.h>
using namespace std;

//Recursive Function
int getSum(int arr[], int index){

   if(index==0)
     return arr[index];

   return arr[index] + getSum(arr, index-1);
}
int main(){

   int arr[] = {10, 20, 30, 50, 89};

   int n = sizeof(arr)/sizeof(arr[0]); 

   cout<<getSum(arr, n-1);
}
Output :
199
