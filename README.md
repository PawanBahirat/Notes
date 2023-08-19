# Project Title

Brief description or tagline about your project.

## Table of Contents

- [Data Structures](#data-structures)
  - [Arrays](#arrays)
    - [Arrays](#arrays)
    - [2D Array](#2d-array)
    - [Remove Even Integers From An Array](#remove-even-integers-from-an-array)
    - [Merge Two Sorted Arrays](#merge-two-sorted-arrays)
    - [Find Two Numbers That Add Up To N](#find-two-numbers-that-add-up-to-n)
    - [Find Minimum Value in Array](#find-minimum-value-in-array)
    - [First Minimum Value In Array](#first-minimum-value-in-array)
    - [Find Second Maximum Value In An Array](#find-second-maximum-value-in-an-array)

## Data Structures

### Arrays
<hr>

- Introduction :

An array also referred to as a collection of elements, is the simplest and most widely used Data Structure. Most of the Data Structures (e.g.Stack and Queue) were derived using the Array structure, which is why it is known as one of the central building blocks of Data Structures. These Data Structures will be discussed later in the coming chapters. The purpose of an Array is to group similar kinds of data for fast access.

Look at the figure below; we have made a simple array with four elements. Each item in the collection is called a Data Element, and the number of data elements stored in an Array is known as its size. You can see that each data element has a maximum of two neighbors, except the first and last one.

- Array Indexing : 

Each data element is assigned a numerical value called the index, which corresponds to the position of that item in the array. It is important to note that the value of the index is non-negative and always starts from zero. So the first element of an array will be stored at index 0 and the last one at index size-1.

An index makes it possible to access the contents of the array directly. Otherwise, we would have to traverse through the whole array to access a single element. That is the key feature that differentiates Arrays from Linked lists (we will cover them in the next chapter).

- Types Of Arrays :

Arrays can store primitive data-type values (e.g., int, char, floats, boolean, byte, short, long, etc.), non-primitive data-type values (e.g., Java Objects, etc.) or it can even hold references of other arrays. That divides the arrays into two categories:

One Dimensional Array
Multi-Dimensional Array
In primitive array, values are stored in a contiguous memory location. Whereas, in the non-primitive array, objects are stored in the heap segment.

- One-Dimensional Array :

The basic syntax for declaring and initializing the one-dimensional array is given below:

- Array Declaration :

In the array declaration, reference of an array is created. To declare an array, you have to specify the data type and name of the array.
```java
datatype arrayName[]; or datatype[] arrayName;
```
Example Program
```java
class OneDArray{ 
    public static void main(String  args[]){
        //Declaration Syntax
        int myArray1[];
        int[] myArray2;
    }
}
```
The above declarations will tell the compiler that reference variables myArray1and myArray2 will hold an array of type int. For now, no actual array exists. To link these reference variables with the actual physical array, we have to create one using the new operator.

- Array Initialization : 

Array initialization actually gives memory to the elements of an array. The basic syntax for initializing an array is given below:
```java
arrayName = new type [size];
```
- Initialization and Declaration in One Step :

We can also declare and initialize the array in one step.
```java
datatype[] arrayName = new datatype [size]; or datatype arrayName[] = new datatype [size];
```
- Practice Problem 👍

[Sum of Array Elements.](https://practice.geeksforgeeks.org/problems/sum-of-array-elements2502/1)

- Adding or Updating Elements in an Array :

To add or update the element in an array, we specify the particular index and assign the new value.
```java
arrayName[index] = value;
```

- How are arrays stored in memory? 

In Java, arrays are dynamically allocated. Arrays are stored in the memory using a reference pointer, which points to the first element. For example, if we create an array of size 3 and name it myArray, then the variable will point to the start of the array. See the figure below:

The only drawback of using arrays is that we have to specify the size of the array during the time of instantiation. That means the size remains fixed and can not be extended. If we want to add more elements, we will have to create a new array, copy all the items from the old array to the new one, and then insert the new element.

### 2D Array
<hr>

- Introduction : 

The Java 2D arrays are arranged as arrays of arrays, i.e., each element of a 2D array is another array. These are generally used if we want to store the data items in a table or matrix-like structure. The representation of the elements is in rows and columns. Thus, we can get a total number of elements in a multidimensional array by multiplying row size with column size.

Like 1D arrays, 2D arrays must have values of the same data type.

- Declaration :
Syntax -
```java
data_type [] [] array_name = new data_type[row_size][column_size];
```
```java
int [][] arr = new int[3][4];
```

This line will create a pointer to store a 2D array. The size of this 2D array is 3 by 4, which means arr holds three 1D arrays, having 4 elements in each.

- Representation of above 2D array in tabular format :
  
| Column 0  | Column 1  | Column 2   | Column 3  |
| :-------  | :-------  | :-------   | :-------  |
| `a[0][0]` | `a[0][1]` | `a[0][2]`  | `a[0][3]` |
| `a[1][0]` | `a[1][1]` | `a[1][2]`  | `a[1][3]` |
| `a[2][0]` | `a[2][1]` | `a[2][2]`  | `a[2][3]` |

- Initialization :
  
There are various ways to initialize a 2D array with values.

The traditional method is to assign values to each element. 
```java
int [][] arr =new int [3][4]; //assigning 10 at Row 2 and Column 1 arr[2][1]=10;
```
We can also initialize it with the declaration itself. 
```java
int[][] arr = { { 1, 2, 3, 4 }, { 5, 6, 7, 8 }, {9, 10, 11, 12} };
```
We can also initialize or assign the values using a loop. 
```java
for (int i = 0; i < 3; i++) { for (int j = 0; j < 4; j++) { arr[i][j]=i+j; } }
```

- Printing 2D array in tabular format :

```java
public class Main {
public static void main(String args[]) {
      int[][] arr = {  { 1, 2, 3, 4 }, 
                   { 5, 6, 7, 8 }, 
                   {9, 10, 11, 12} };
                   
     for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 4; j++) {
 	    	 System.out.print(arr[i][j]+" ");
        }  
        System.out.println();
     }
}
}
```

- Practice Problems 👍

[Sum of Elements in a matrix.](https://practice.geeksforgeeks.org/problems/sum-of-elements-in-a-matrix2000/1)

[Diagonal Sum.](https://practice.geeksforgeeks.org/problems/diagonal-sum0158/1)

[Multiply Matrices.](https://practice.geeksforgeeks.org/problems/multiply-matrices/1)

[Transpose of Matrix.](https://practice.geeksforgeeks.org/problems/transpose-of-matrix-1587115621/1)

[Rotate by 90 degree.](https://practice.geeksforgeeks.org/problems/rotate-by-90-degree-1587115621/1)


### Remove Even Integers From An Array
<hr>

Given an array of size n, remove all even integers from it. Implement this solution in Java and see if it runs without an error.

In this problem, you have to implement the `int [] removeEven(int[] arr)` method, which removes all the even elements from the array and returns back updated array.

- Method Prototype :
```java
int[] removeEven(int[] arr);
```
- Input :
An array with integers.

- Output :
An array with only odd integers.

- Sample Input :
```java
arr = {1, 2, 4, 5, 10, 6, 3}
```
- Sample Output :
```java
arr = {1, 5, 3}
```
**SOLUTION**
- CODE :
```java
class CheckRemoveEven {
  
	public static int[] removeEven(int[] arr) {
		int oddElements = 0;

		//Find number of odd elements in arr
		for (int i = 0; i < arr.length; i++) {
			if (arr[i] % 2 != 0) oddElements++;
		}

		//Create result array with the size equal to the number of odd elements in arr
		int[] result = new int[oddElements];
		int result_index = 0;

		//Put odd values from arr to the resulted array
		for (int i = 0; i < arr.length; i++) {
			if (arr[i] % 2 != 0) 
        result[result_index++] = arr[i];
		} //end of for loop

		return result;
	} //end of removeEven


  public static void main(String args[]) {
  
    int size = 10;
    int[] arr = new int[size]; //declaration and instantiation 
  
    System.out.print("Before removing Even Numbers: "); 
    for (int i = 0; i < arr.length; i++) {
      arr[i] = i; // assigning values
      System.out.print(arr[i] +  " ");
    }
    System.out.println();
  
    int[] newArr =  removeEven(arr); // calling removeEven
  
    System.out.print("After removing Even Numbers: "); 
    for (int i = 0; i < newArr.length; i++) {
      System.out.print(newArr[i] +  " "); // prinitng array
    }
  }
}
```
- Explanation :

This solution first finds the number of odd elements in the given array by iterating over it and incrementing a count variable if an element is odd.

Next, we initialize an array with a size oddElements, and store all the odd numbers in it.

- Time Complexity :

Since the entire array has to be iterated over, this solution is in O(n).

### Merge Two Sorted Arrays
<hr>

- Problem Statement :
In this problem, given two sorted arrays, you have to implement the `int[] mergeArrays(int[] arr1, int[] arr2)` method, which returns an array consisting of all elements of both arrays in a sorted way.

- Method Prototype :
```java
int[] mergeArrays(int[] arr1, int[] arr2)
```
Here arr1 and arr2 are sorted already.

- Sample Input :
```java
arr1 = {1, 3, 4, 5}
arr2 = {2, 6, 7, 8}
```
- Sample Output :
```java
arr = {1, 2, 3, 4, 5, 6, 7, 8}
````
**SOLUTION**
- CODE :
```java
class checkMergeArray { 

  // Merge arr1 and arr2 into resultantArray
  public static int[] mergeArrays(int[] arr1, int[] arr2) { 
    int s1 = arr1.length;
    int s2 = arr2.length;
    int[] resultantArray = new int[s1+s2];
    int i = 0, j = 0, k = 0;

    // Traverse both array 
    while (i < s1 && j < s2) { 
      // Check if current element of first 
      // array is smaller than current element 
      // of second array. If yes, store first 
      // array element and increment first array 
      // index. Otherwise do same with second array 
      if (arr1[i] < arr2[j]) 
        resultantArray[k++] = arr1[i++]; 
      else
        resultantArray[k++] = arr2[j++]; 
    } 

    // Store remaining elements of first array 
    while (i < s1) 
      resultantArray[k++] = arr1[i++]; 

    // Store remaining elements of second array 
    while (j < s2) 
      resultantArray[k++] = arr2[j++]; 

    return resultantArray;
  } 

  public static void main(String args[]) {

    int[] arr1 = {1,12,14,17,23}; // creating a sorted array called arr1
    int[] arr2 = {11,19,27};  // creating a sorted array called arr2

    int[] resultantArray = mergeArrays(arr1, arr2); // calling mergeArrays

    System.out.print("Arrays after merging: ");
    for(int i = 0; i < arr1.length + arr2.length; i++) {
      System.out.print(resultantArray[i] + " ");
    }
  }
}
```
- Explanation : 

In the solution above, we start by creating a new empty array of the size equal to the sum of sizes of input arrays. Starting off from the index 0 individually compare the elements at corresponding indexes of both arrays. Place the element with smaller value in the resultant array, and increment the index of the array where you find the smallest element. Keep repeating this till you hit the end of one array. Move the elements of the other array into the resultantArray as it is.

Now you’ve got the sorted resultantArray!

- Time Complexity :

The time complexity for this algorithm is O(n+m), where nn and mm are the sizes of arr1 and arr2, respectively. This is because both arrays are iterated over once.

### Find Two Numbers That Add Up To N
<hr>

- Problem statement :

Implement a function that takes an array `arr`, a number `value`, and the `size` of the array as an input and returns two numbers which add up to `value`.

- Input :

The input is an array, a value, and the size of the array

- Output :

An array with two integers that add up to the value given

- Sample input :
```java
arr = {1,21,3,14,5,60,7,6}; value = 81;
```
- Sample output :
```java
arr = {21,60};
```
For example, in this illustration we are given 81 as the number value. When we traverse the whole array, we find that 21 and 60 are the integers that add up to 81.

**Soluion: Using quicksort**
- Code :
```java
Helper.java

import java.util.Random;

class Helper {
 static void swap(int[] array, int i, int j) {
  int temp = array[i];
  array[i] = array[j];
  array[j] = temp;
 }
 public static int choosePivot(int left, int right) {
  Random rand = new Random();
  // Pick 3 random numbers within the range of the array
  int i1 = left + (rand.nextInt(right - left + 1));
  int i2 = left + (rand.nextInt(right - left + 1));
  int i3 = left + (rand.nextInt(right - left + 1));

  // Return their median
  return Math.max(Math.min(i1, i2), Math.min(Math.max(i1, i2), i3));
 }

 public static int partition(int arr[], int left, int right) {
  int pivotInd = choosePivot(left, right); // Index of pivot
  swap(arr, right, pivotInd); // self created function to swap two indices of an array
  int pivot = arr[right]; // Pivot 
  int i = (left - 1); // All the elements less than or equal to the
  // pivot go before or at i

  for (int j = left; j <= right - 1; j++) {
   if (arr[j] <= pivot) {
    i++; // increment the index 
    swap(arr, i, j);
   }
  }
  swap(arr, i + 1, right); // Putting the pivot back in place
  return (i + 1);
 }

 public static void quickSort(int arr[], int left, int right) {
  if (left < right) {
   // pi is where the pivot is at
   int pi = partition(arr, left, right);

   // Separately sort elements before and after partition 
   quickSort(arr, left, pi - 1);
   quickSort(arr, pi + 1, right);
  }
 }
}
main.java

class CheckSum {
 static Helper obj = new Helper();

 public static int[] findSum(int[] arr, int n) //Returns 2 elements of arr that sum to the given value
 {
  //Helper sort function that uses the Quicksort Algorithm
  obj.quickSort(arr, 0, arr.length - 1); //Sort the array in Ascending Order

  int Pointer1 = 0; //Pointer 1 -> At Start
  int Pointer2 = arr.length - 1; //Pointer 2 -> At End

  int[] result = new int[2];
  int sum = 0;

  while (Pointer1 != Pointer2) {

   sum = arr[Pointer1] + arr[Pointer2]; //Calulate Sum of Pointer 1 and 2

   if (sum < n)
    Pointer1++; //if sum is less than given value => Move Pointer 1 to Right
   else if (sum > n)
    Pointer2--;
   else {
    result[0] = arr[Pointer1];
    result[1] = arr[Pointer2];
    return result; // containing 2 number 
   }
  }
  return arr;
 }

 public static void main(String args[]) {

  int n = 9;
  int[] arr1 = {2, 4, 5, 7, 8};
  int[] arr2 = findSum(arr1, n);
  int num1 = arr2[0];
  int num2 = arr2[1];

  if ((num1 + num2) != n)
   System.out.println("Results not found!");
  else
   System.out.println("Sum of " + n + " found: " + num1 + " and " + num2);
 }
}
```
While solution #1 is very intuitive, it is not very time efficient. A better way to solve this challenge is by first sorting the array, then using two variables: one starting from the first index of the array and the second starting from the last index of the array, (size-1size−1).

If the sum of the elements at these indices of the array is smaller than the given value, then we increment Pointer1. If the sum is smaller, then we decrement Pointer2 from the end. If none of those conditions are true, this means that the sum is equal to the given value. That being said, we will append the elements at those indices in the array and return the result.

- Time complexity :
Since the sorting function we use in this code takes O(nlog(n)) and the algorithm itself takes O(n) time, the overall time complexity of this algorithm is in O(nlog(n)).

**Solution: Use hashing**
```java
class CheckSum {
 public static int[] findSum(int[] arr, int n) {
  int[] result = new int[2];
  HashMap < Integer, Boolean > hmap = new HashMap < Integer, Boolean > (); // Create a hashmap

  for (int i = 0; i < arr.length; i++) {
   if (hmap.containsKey(arr[i])) // If a value from arr is present in hmap
   {
    result[0] = arr[i];
    result[1] = n - arr[i];
    return result;
   }
   else
   hmap.put(n - arr[i], true); // Store value - arr[i] if element is not present in arr
  }
  return result;
 }

 public static void main(String args[]) {

  int n = 9;
  int[] arr1 = {2, 4, 5, 7, 8};
   int[] arr2 = findSum(arr1, n);
  int num1 = arr2[0];
  int num2 = arr2[1];

  if ((num1 + num2) != n)
   System.out.println("Results not found!");
  else
   System.out.println("Sum of " + n + " found: " + num1 + " and " + num2);
 }
}
```

- Explanation :

We solve this problem by using a HashMap called `hmap`.

We will run a `for` loop on the whole array. If the element `arr[i]` doesn’t exist in the hmap, we add `n - arr[i]` to the `hmap` as shown in the line 14.

If any element of `arr` exists in the `hmap`, that means the difference of `n` and the number found `(n - arr[i])` are also present.

Therefore, an array of size 2 called `result` is created to store the pair that sums up to `n`. If `hmap` contains any array element, `result[]` is updated, or else it is returned containing the default value.

- Time complexity :

This code works in O(n), as the whole array is iterated over once.

### Find Minimum Value in Array
<hr>

- Problem Statement :

In this problem, you have to implement the int findMinimum(int[] arr) method, which will traverse the whole array and find the smallest number in the array.

- Method Prototype :

int findMinimum(int[] arr) Here arr1 and arr2 are sorted already.

- Sample Input :
```java
arr = {9, 2, 3, 6}
```
- Sample Output :
```java
2
```
**SOLUTION**
- CODE :
```java
public static int findMinimum(int[] arr) {

    int minimum = arr[0];

    //At every Index compare its value with minimum and if its less 
    //then make that index value new minimum value
    for (int i = 1; i < arr.length; i++) {

      if (arr[i] < minimum) {
        minimum = arr[i];
      }
    }
    return minimum;
  }
```
- Explanation :

Start with the first element, which is 9 in this example, and save it in minimum as the smallest value. Then, iterate over the rest of the array and compare the minimum to each element. If any element is smaller than the minimum, then set the minimum to that element. By the end of the array, the number stored in the minimum will be the smallest integer in the whole array.

- Time Complexity :

Since the entire list is iterated over once, this algorithm is in linear time, O(n).






### First Minimum Value In Array

Description and usage instructions for "First Minimum Value In Array" problem.

### Find Second Maximum Value In An Array

Description and usage instructions for "Find Second Maximum Value In An Array" problem.

## Contributing

... (rest of your README)
