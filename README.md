# DSA (Data structures & Algorithms)

- [Data Structures](#data-structures)
  - [Arrays](#arrays)
    - [Arrays](#arrays)
    - [2D Array](#2d-array)
    - [Remove Even Integers From An Array](#remove-even-integers-from-an-array)
    - [Merge Two Sorted Arrays](#merge-two-sorted-arrays)
    - [Find Two Numbers That Add Up To N](#find-two-numbers-that-add-up-to-n)
    - [Find Minimum Value in Array](#find-minimum-value-in-array)
    - [First Non-Repeating Integer In An Array](#first-non-repeating-integer-in-an-array)
    - [Find Second Maximum Value In An Array](#find-second-maximum-value-in-an-array)
    - [Find The Sum Of Maximum Sum Subarray](#find-the-sum-of-maximum-sum-subarray)
    - [Binary Search](#binary-search-on-sorted-array)
    - [Find Maximum In Sliding Window](#find-maximum-in-sliding-window)
    - [Move All Zeroes to the Beginning of the Array](#move-all-zeroes-to-the-beginning-of-the-array)
    - [Stock Buy Sell to Maximize Profit](#stock-buy-sell-to-maximize-profit)
    - [Sort an Array Using Quicksort Algorithm](#sort-an-array-using-quicksort-algorithm)
    - [Maximum Sum Subarray Of Size K](#maximum-sum-subarray-of-size-k)
  - [Strings](#strings)
    - [Strings](#strings)
    - [Reverse Words in a Sentence](#reverse-words-in-a-sentence)
    - [Remove Duplicates from a String](#remove-duplicates-from-a-string)
    - [Remove White Spaces from a String](#remove-white-spaces-from-a-string)
    - [Word Break Problem](#word-break-problem)
    - [Find all Palindrome Substrings](#find-all-palindrome-substrings)
    - [Balanced Parentheses](#balanced-parentheses)
    - [Longest Substring with Distinct Characters](#longest-substring-with-distinct-characters)
  - [Linked List](#linked-list)
    - [Introduction To Linked Lists](#introduction-to-linked-lists)
    - [Insertion In a Singly Linked List (insert at End)](#insertion-in-a-singly-linked-list-insert-at-end)
    - [Search In Singly Linked List](#search-in-singly-linked-list)
    - [Deletion In Singly Linked List (delete By Value)](#deletion-in-singly-linked-list-delete-by-value)
    - [Linked Lists Vs Arrays](#linked-lists-vs-Arrays)
    - [Find The Length Of A Linked List](#find-the-length-of-a-linked-list)
    - [Reverse A Linked List](#reverse-a-linked-list)
    - [Detect Loop In A Linked List](#detect-loop-in-a-linked-list)
    - [Find The Middle Node Of A Linked List](#find-the-middle-node-of-a-linked-list)
    - [Remove Duplicates From A Linked List](#remove-duplicates-from-a-linked-list)
    - [Return The Nth Node From End](#return-the-nth-node-from-end)
    - [Implementation Of Linked List](#implementation-of-linked-list)
    - [Intersection Point Of Two Lists](#intersection-point-of-two-lists)
    - [Reverse Alternate K Nodes In A Singly Linked List](#reverse-alternate-k-nodes-in-a-singly-linked-list)
    - [Merge K Sorted Lists](#merge-k-sorted-lists)
  - [Stack and Queues](#stack-and-queues)
    - [Introduction To Stacks and Queues](#introduction-to-stacks-and-queues)
    - [Implementation Of Stack](#implementation-of-stack)
    - [Implementation Of Queue](#implementation-of-queue)
    - [Implement Queue Using Stacks](#implement-queue-using-stacks)
    - [Implement Queue Using Stacks (1)](#implement-queue-using-stacks-1)
    - [Reversing The First K Elements Of A Queue](#reversing-the-first-k-element-of-a-queue)
    - [Evaluate Postfix Expressions Using Stacks](#evaluate-postfix-expressions-using-stacks)
    - [Next Greater Element Using Stackproblem Statement](#next-greater-element-using-stack)
    - [Solve A Celebrity Problem Using A Stack](#solve-a-celebrity-problem-using-a-stack)
    - [Check For Balanced Parentheses Using A Stack](#check-for-balanced-parantheses-using-a-stack)
    - [Create Stack Where Min() Gives Minimum In Constant Time](#create-stack-where-min-gives-minimum-in-constant-time)

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
- Example Program :
- Code :tada:
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
- Code :tada:
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
- Code :tada:
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
- Code :tada:
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
- Code :tada:
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
Since the sorting function we use in this Code takes O(nlog(n)) and the algorithm itself takes O(n) time, the overall time complexity of this algorithm is in O(nlog(n)).

**Solution: Use hashing**
- Code :tada:
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

This Code works in O(n), as the whole array is iterated over once.

### Find Minimum Value in Array
<hr>

- Problem Statement :

In this problem, you have to implement the `int findMinimum(int[] arr)` method, which will traverse the whole array and find the smallest number in the array.

- Method Prototype :

`int findMinimum(int[] arr)` Here arr1 and arr2 are sorted already.

- Sample Input :
```java
arr = {9, 2, 3, 6}
```
- Sample Output :
```java
2
```
**SOLUTION**
- Code :tada:
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

### First Non Repeating Integer In An Array
<hr>

- Problem Statement :

In this problem, you have to implement the `int findFirstUnique(int[] arr)` function that will look for a first unique integer which appears only once in the whole array. You must use hashing to implement this function in the most optimized way possible.
```
Note: We consider zero to be an integer for the premise of this challenge.
```
- Function Prototype :
```java
int findFirstUnique(int[] arr)
```
- Output :

The first unique element in the array.

- Sample Input :
```java
arr = {9, 2, 3, 2, 6, 6}
```
- Sample Output :
```java
9
```
**Solution: Using a HashMap**
- Code :tada:
```java
class CheckFirstUnique {
    public static int findFirstUnique(int[] arr) {

        Map<Integer, Integer> countElements = new HashMap<>();
        //If the element does not exist in the HashMap
        //Add that element with value = 0
        //or else update the number of occurrences of that element by adding 1
        for (int i = 0; i < arr.length; i++) {
            if(countElements.containsKey(arr[i])){
                int occurence = countElements.get(arr[i]) + 1;
                countElements.put(arr[i], occurence);
            }
            else
                countElements.put(arr[i], 0); 
        }
        //Traverse the array and check the number of occurrences
        //Return the first element with 0 occurences
        for (int i = 0; i < arr.length; i++) {
            if (countElements.get(arr[i]) == 0) {
                return arr[i];
            }
        }
        //If no such element is found, return -1
        return -1;
    }

    public static void main(String args[]) {

        int[] arr = {2, 54, 7, 2, 6, 54};

        System.out.println("Array: " + Arrays.toString(arr));

        int unique = findFirstUnique(arr);
        System.out.print("First Unique in an Array: " + unique);

    }
}
```
- Explanation :

Firstly, we store all the elements from the array into a `HashMap`. The element is stored as `key` and the count of multiple occurrences is stored as `value` in the `HashMap`. Initially, the count is 0. But if the same element is encountered again, the count is increased by `1` each time.

Afterward, we traverse the array again from the beginning and return the first element which has count equal to `0` in the `HashMap`.

- Time Complexity :

The array is iterated multiple times but the complexity is still linear. The time complexity of this Code is O(n).

**Solution: Using a TreeMap**
- Code :tada:
  
```java
class CheckFirstUnique {
    public static int findFirstUnique(int[] arr) {

        Map<Integer, Integer> countElements = new TreeMap<>(); //TreeMap is sorted
        //If the element does not exist in the TreeMap
        //Add that element with value = 0
        //or else update the number of occurrences of that element by adding 1
        for (int i = 0; i < arr.length; i++) {
            if(countElements.containsKey(arr[i])){
                int occurence = countElements.get(arr[i]) + 1;
                countElements.put(arr[i], occurence);
            }
            else
                countElements.put(arr[i], 0); 
        }
        //Traverse the array and check the number of occurrences
        //Return the first element with 0 occurences
        for (int i = 0; i < arr.length; i++) {
            if (countElements.get(arr[i]) == 0) {
                return arr[i];
            }
        }
        //If no such element is found, return -1
        return -1;
    }

    public static void main(String args[]) {

        int[] arr = {2, 54, 7, 2, 6, 54};

        System.out.println("Array: " + Arrays.toString(arr));

        int unique = findFirstUnique(arr);
        System.out.print("First Unique in an Array: " + unique);

    }
}
```
- Time Complexity :

The time complexity of this program is O(n).

### Find Second Maximum Value In An Array
<hr>

- Problem Statement :

In this problem, you have to implement the `int findSecondMaximum(int[] arr)` method, which will traverse the whole array and return the second largest element present in the array.

- Assumption :
 
Array should contain at least two unique elements.

- Method Prototyp :
```java
int findSecondMaximum(int[] arr)
```
- Sample Input :
```java
arr = {9,2,3,6}
```
- Sample Output :
```java
6
```
**SOLUTION**
- Code :tada:
```java
public static int findSecondMaximum(int[] arr) {

    int max = Integer.MIN_VALUE;;
    int secondmax = Integer.MIN_VALUE;

    // Keep track of Maximum value, whenever the value at an array index is greater
    // than current Maximum value then make that max value 2nd max value and
    // make that index value maximum value  
    for (int i = 0; i < arr.length; i++) {
      if (arr[i] > max) {
        secondmax = max;
        max = arr[i];
      }
      else if (arr[i] > secondmax && arr[i] != max) {
        secondmax = arr[i];
      }
    }//end of for-loop

    return secondmax;
  }
  ```
- Explanation :

We initialize two variables `max` and `secondmax` to Integer. MIN_VALUE having value `-2147483648`, which is the maximum integer negative value range. We then traverse the array, and if the current element in the array is greater than the maximum value, then set `secondmax` to `max` and `max` to the current element. If the current element is greater than the `secondmax` but less than max, then update `secondmax` to store the value of the current element. Finally, return the value stored in `secondmax`.

- Time Complexity :

This solution is in O(n) since the list is traversed once only.

### Find The Sum Of Maximum Sum Subarray
<hr>

- Problem Statement :

Given an integer array, return the maximum subarray sum. The array may contain both positive and negative integers and is unsorted.

- Method Prototype :
```java
int findMaxSumSubArray(int[] arr)
```
- Sample Input :
```java
arr = {1, 7, -2, -5, 10, -1}
```
- Sample Output :
```java
11
```

**Kadane's Algorithm**
- Code :tada:
```java
public static int findMaxSumSubArray(int[] arr) {
        if (arr.length < 1) {
            return 0;
        }

        int currMax = arr[0];
        int globalMax = arr[0];
        int lengtharray = arr.length;
        for (int i = 1; i < lengtharray; i++) {
            if (currMax < 0) {
            currMax = arr[i];
            } else {
            currMax += arr[i];
            }

            if (globalMax < currMax) {
            globalMax = currMax;
            }
        }
        return globalMax;
    }
```
- Explanation :

The basic idea of Kadane’s algorithm is to scan the entire array and at each position find the maximum sum of the subarray ending there. This is achieved by keeping a currMax for the current array index and a globalMax. The algorithm is as follows:
```java
 currMax = A[0]
globalMax = A[0]
for i = 1 -> size of A
    if currMax is less than 0
        then currMax = A[i]
    otherwise 
        currMax = currMax + A[i]
    if globalMax is less than currMax 
        then globalMax = currMax
```

- Time Complexity :

The runtime complexity of this solution is linear, O(n).

### Binary Search on Sorted Array
<hr>

- Description :

Given a sorted array of integers, return the index of the given key. Return `-1` if the key is not found.

- Example : 

Given the following array, if the search key is `47`, binary search will return `3`.

![image](https://github.com/PawanBahirat/Notes/assets/99033177/e83ca0c0-1e65-4536-88b7-da46e32c0543)

- Explanation :

Binary search is used to find the index of an element in a sorted array. If the element doesn’t exist, that can be determined efficiently as well. The algorithm divides the input array by half at every step. After every step, either we have found the index that we are looking for or half of the array can be discarded. Hence, the solution can be calculated in O(log n) time.

Here’s how the algorithm works:

At every step, consider the array between `low` and `high` indices
Calculate the `mid` index.
If the element at the `mid` index is the `key`, return `mid`.
If the element at `mid` is greater than the `key`, then change the index `high` to `mid - 1`. The index at `low` remains the same.
If the element at `mid` is less than the `key`, then change `low` to `mid + 1`. The index at high remains the same.
When `low` is greater than `high`, the `key` doesn’t exist and -1 is returned.

- Code :tada:
```java
static int binSearch(int[] A, int key) {
  
    int low = 0;
    int high = A.length -1;

    while (low <= high) {

      int mid = low + ((high - low) / 2);

      if (A[mid] == key) {
        return mid;
      }

      if (key < A[mid]) {
        high = mid - 1;
      }
      else {
        low = mid + 1;
      }
    }
    return -1;
  }
```

### Find Maximum In Sliding Window
<hr>

- Description :

Given a large array of integers and a window of size ww, find the current maximum value in the window as the window slides through the entire array.

Let’s try to find all maximums for a window size equal to 33 in the array given below :

`-4`	`2`	`-5`	`3`	`6`

- Step1 : For the first 3 elements in the window, max is 2.

`-4`	`2`	`-5`

- Step2 : Slide window one position to the right and max for window becomes 3.

`2`	`-5`	`3`

- Step3 : In the last window, max is 6.

`-5`	`3`	`6`

- Solution Approach :

The algorithm uses the deque data structure to find the maximum in a window. A deque is a double-ended queue in which push and pop operations work in O(1) at both ends. It will act as our window. At the start of the algorithm, we search for the maximum value in the first window. The first element’s index is pushed to the front of the deque. If an element is smaller than the one at the back of the queue, then the index of this element is pushed in and becomes the new back. If the current element is larger, the back of the queue is popped repeatedly until we can find a higher value, and then we’ll push the index of the current element in as the new back. As we can see, the deque stores elements in decreasing order. The front of the deque contains the index for the maximum value in that particular window. We will repeat the following steps each time our window moves to the right:

Remove the indices of all elements from the back of the deque, which are smaller than or equal to the current element.
If the element no longer falls in the current window, remove the index of the element from the front.
Push the current element index at the back of the window.
The index of the current maximum element is at the front.

- Code :tada:
```java
 public static ArrayDeque<Integer> findMaxSlidingWindow(int[] arr, int windowSize) {

    ArrayDeque<Integer> result = new ArrayDeque<>(); // ArrayDeque for storing values
    Deque<Integer> list = new LinkedList<Integer>(); // creating a linked list

    if(arr.length > 0) {

      if( arr.length < windowSize) // Invalid State
        return result;

      for(int i = 0; i < windowSize; ++i) {
        // Removing last smallest element index
        while(!list.isEmpty() && arr[i] >= arr[list.peekLast()]){
          list.removeLast();      
        }
         
        // Adding newly picked element index
        list.addLast(i);
      }

      for(int i = windowSize; i < arr.length; ++i) {
        result.add(arr[list.peek()]);

        // Removing all the elements indexes which are not in the current window
        while((!list.isEmpty()) && list.peek() <= i-windowSize)
          list.removeFirst();

        // Removing the smaller elements indexes which are not required
        while((!list.isEmpty()) && arr[i] >= arr[list.peekLast()])
          list.removeLast();

        // Adding newly picked element index
        list.addLast(i);
      }

      // Adding the max number of the current window in the result
      result.add(arr[list.peek()]);
      return result; // returning result
    }
    else 
      return result;
  }
```

### Move All Zeroes to the Beginning of the Array
<hr>

- Description :

Given an integer array, move all elements that are 0 to the left while maintaining the order of other elements in the array. The array has to be modified in-place. Let’s look at the following integer array:

`1`	`10`	`20`	`0`	`59`	`63`	`0`	`88`	`0`

After moving all zeros to the left, the array should look like this:

`0`	`0`	`0`	`1`	`10`	`20`	`59`	`63`	`88`

Remember : We need to maintain the order of non-zero elements.

- Solution Approach :

We will keep two markers: `read_index` and `write_index` and point them to the end of the array. Let’s take a look at an overview of the algorithm: While moving `read_index` towards the start of the array:

If `read_index` points to `0`, skip.
If `read_index` points to a non-zero value, write the value at `read_index` to `write_index` and decrement `write_index`.
Assign zeros to all the values before the `write_index` and to the current position of `write_index` as well.

- Code :tada:
```java
static void moveZerosToLeft(int[] A) {
    if (A.length < 1) {
      return;
    }

    int writeIndex = A.length - 1;
    int readIndex = A.length - 1;

    while(readIndex >= 0) {
      if(A[readIndex] != 0) {
        A[writeIndex] = A[readIndex];
        writeIndex--;
      }

      readIndex--;
    }

    while(writeIndex >= 0) {
      A[writeIndex] = 0;
      writeIndex--;
    }
  }
```
- Runtime complexity :

The runtime complexity if this solution is linear, O(n).

- Memory complexity :

The memory complexity of this solution is constant, O(1).

### Stock Buy Sell to Maximize Profit
<hr>

- Description :
  
Given a list of daily stock prices (integers for simplicity), return the buy and sell prices for making the maximum profit.

We need to maximize the single buy/sell profit. If we can’t make any profit, we’ll try to minimize the loss. For the below examples, buy and sell prices for making a maximum profit are highlighted.

`8`	`5`	`12`	`9`	`19`	`1`

- Solution Approach :

The values in the array represent the cost of a stock each day. As we can `buy` and `sell` the stock only once, we need to find the best `buy and sell` prices for which our profit is maximized (or loss is minimized) over a given span of time.

A naive solution, with runtime complexity of O(n^2), is to find the maximum gain between each element and its succeeding elements. There is a tricky linear solution to this problem that requires maintaining `current_buy_price` (which is the smallest number seen so far), `current_profit`, and `global_profit` as we iterate through the entire array of stock prices. At each iteration, we will compare the `current_profit` with the `global_profit` and update the `global_profit` accordingly. The basic algorithm is as follows:

```
current profit = INT_MIN
current buy = stock_prices[0]
global sell = stock_prices[1]
global profit = global sell - current buy

for i = 1 to stock_prices.length:
  current profit = stock_prices[i] - current buy
  if current profit is greater than global profit 
    then update global profit to current profit and update global sell to stock_prices[i]
  if stock_prices[i] is less than current buy 
    then update current buy to stock_prices[i]

return global profit and global sell
```

- Code :tada:
```java
class Tuple<X, Y> {             
  public X x; 
  public Y y; 

  public Tuple(X x, Y y) { 
    this.x = x; 
    this.y = y; 
  } 
}

public static Tuple findBuySellStockPrices(int[] array) {
    if(array == null || array.length < 2) {
        return null;
      }

    int current_buy = array[0];
    int global_sell = array[1];
    int global_profit = global_sell - current_buy;

    int current_profit = Integer.MIN_VALUE;
  
    for(int i=1; i<array.length; i++) {
      current_profit = array[i] - current_buy;
  
      if(current_profit > global_profit) {
        global_profit = current_profit;
        global_sell = array[i];
      }

      if(current_buy > array[i]) {
        current_buy = array[i];
      }
    }

    Tuple<Integer, Integer> result = 
      new Tuple<Integer, Integer>(global_sell - global_profit, global_sell);

    return result;
  }
```
- Runtime complexity :

The runtime complexity if this solution is linear, O(n).

- Memory complexity :

The memory complexity of this solution is constant, O(1).

### Sort an Array Using Quicksort Algorithm
<hr>

- Description :

Given an integer array, sort it in ascending order using the quicksort algorithm.

- Original Array :

`55`	`23`	`26`	`2`	`25`

- Sorted Array :

`2`	`23`	`25`	`26`	`55`

- Solution Approach :

Here is an overview of how the quicksort algorithm works :

Select a pivot element from the array to divide the array into two parts based on the pivot. We pick the first element as the pivot.
Reorder the array by comparing with the pivot element such that smaller values end up at the left side, and larger values end up at the right side of the pivot.
Now, the pivot element is in its correct sorted position. Applying the above steps, we can recursively sort the sublists on the right and left sides of the pivot.

Code :tada:
```java
  static int partition(int[] arr, int low, int high) {
    int pivotValue = arr[low];
    int i = low;
    int j = high;

    while (i < j) {
      while (i <= high && arr[i] <= pivotValue) i++;
      while (arr[j] > pivotValue) j--;

      if (i < j) {
        // swap arr[i] and arr[j]
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
      }
    }

    arr[low] = arr[j];
    arr[j] = pivotValue;
  
    // return the pivot index
    return j;
  }

  static void quickSortRec(int[] arr, int low, int high) {
    if (high > low) {
      int pivotIndex = partition(arr, low, high);

     quickSortRec(arr, low, pivotIndex - 1);
      quickSortRec(arr, pivotIndex + 1, high);
    }
  }

  static void quickSort(int[] arr) {
    quickSortRec(arr, 0, arr.length - 1);
  }
```

- Runtime complexity :

The runtime complexity of this solution is linearithmic, O(nlogn).

- Memory complexity :

The memory complexity of this solution is logarithmic, O(logn).

### Maximum Sum Subarray of Size K
<hr>

- Description :

Given an array of positive numbers and a positive number ‘k,’ find the maximum sum of any contiguous subarray of size ‘k’.

- Example 1 :
```
Input: [2, 1, 5, 1, 3, 2], k=3 Output: 9 Explanation: Subarray with maximum sum is [5, 1, 3].
```
- Example 2 :
```
Input: [2, 3, 4, 1, 5], k=2 Output: 7 Explanation: Subarray with maximum sum is [3, 4].
```
- Solution Approach :

A basic brute force solution will be to calculate the sum of all ‘k’ sized subarrays of the given array to find the subarray with the highest sum. We can start from every index of the given array and add the next ‘k’ elements to find the subarray’s sum.

- Code :tada:
```java
public static int findMaxSumSubArray(int k, int[] arr) {
    int maxSum = 0, windowSum;
    for (int i = 0; i <= arr.length - k; i++) {
      windowSum = 0;
      for (int j = i; j < i + k; j++) {
        windowSum += arr[j];
      }
      maxSum = Math.max(maxSum, windowSum);
    }

    return maxSum;
  }
```
The above algorithm’s time complexity will be O(N*K)O(N∗K), where ‘N’ is the total number of elements in the given array. Is it possible to find a better algorithm than this?

- A better approach :

If you observe closely, you will realize that to calculate the sum of a contiguous subarray, we can utilize the sum of the previous subarray. For this, consider each subarray as a Sliding Window of size ‘k.’ To calculate the sum of the next subarray, we need to slide the window ahead by one element. So to slide the window forward and calculate the sum of the new position of the sliding window, we need to do two things:

Subtract the element going out of the sliding window, i.e., subtract the first element of the window.
Add the new element getting included in the sliding window, i.e., the element coming right after the end of the window.
This approach will save us from re-calculating the sum of the overlapping part of the sliding window. Here is what our algorithm will look like:

- Code :tada:
```java
public static int findMaxSumSubArray(int k, int[] arr) {
   int windowSum = 0, maxSum = 0;
   int windowStart = 0;
   for (int windowEnd = 0; windowEnd < arr.length; windowEnd++) {
     windowSum += arr[windowEnd]; // add the next element
     // slide the window, we don't need to slide if we've not hit the required window size of 'k'
     if (windowEnd >= k - 1) {
       maxSum = Math.max(maxSum, windowSum);
       windowSum -= arr[windowStart]; // subtract the element going out
       windowStart++; // slide the window ahead
     }
   }

   return maxSum;
 }
 ```
- Runtime complexity :

The time complexity of the above algorithm will be O(N).

- Memory complexity :

The algorithm runs in constant space O(1).

### Strings
<hr>

- Common Methods & Operations :

A cheat sheet of common methods and operations on strings. Take a look at the table below that lists some common operations that can be performed on a string using built-in methods.

| Method | Description |
| --- | --- |
| str.length() | Returns the length of the string str |
| str.charAt(n) | Returns the character at the specified index |
| str.indexOf(ch) | Returns the index of the first occurrence of character ch in the string. |
| str.substring(start, end) | Returns a new string which is a substring of str beginning at start and extends to end-1 |
| str.substring(start, end) | Returns a new string which is a substring of str beginning at start and extends to end-1 |
| str.toLowerCase() | Converts string str to lower case |
| str.toUpperCase() | Converts string str to upper case |
| str1.equals(str2) | Compares the str1 with the str2 and returns true if both matches else false. |
| str1.compareTo(str2) | Returns 0 if the str1 is equal to str2, negative value if the str1 is lexicographically less than str2 or value greater than 0 if the str1 is lexicographically greater than str2|
| str.split(regex) | Splits the string and returns the array of substrings that matches the given regular expression. |
| str1.contains(str2) | Returns true if str2 is found in string str1 |
| str1.concat(str2) | Combines strings str1 and str2 |
	
### Reverse Words in a Sentence
<hr>

Given a sentence (an array of characters), reverse the order of words.

- Description- :

Reverse the order of words in a given sentence (an array of characters). Take the “Hello World” string for example:
```
The "Hello World" string reversed should be "World Hello".
```
- Solution :

Here is how the solution works:

Reverse the string.
Traverse the string and reverse each word in place.
Let’s apply this solution to our example:
```
“The quick brown fox jumped over the lazy dog.”.
```
Reverse the string: “.god yzal eht revo depmuj xof nworb kciuq ehT”
Reverse each word in-place: “dog. lazy the over jumped fox brown quick The”

- Code :tada:
```java

class ReverseWords {
  // Null terminating strings are not used in java
  public static void strRev(char[] str, int start, int end) {
    if (str == null || str.length < 2) {
      return;
    }

    while (start < end) {
      char temp = str[start];
      str[start] = str[end];
      str[end] = temp;
      start++;
      end--;
    }
  }

  public static void reverseWords(char[] sentence) {
    // Here sentence is a null-terminated string ending with char '\0'.
    if (sentence == null || sentence.length == 0) {
      return;
    }

    // To reverse all words in the string, we will first reverse
    // the string. Now all the words are in the desired location, but
    // in reverse order: "Hello World" -> "dlroW olleH".
    int len = sentence.length;
    strRev(sentence, 0, len - 2);

    // Now, let's iterate the sentence and reverse each word in place.
    // "dlroW olleH" -> "World Hello"
    int start = 0;
    int end;

    while (true) {
      // find the  start index of a word while skipping spaces.
      while (sentence[start] == ' ') {
        ++start;
      }

      if (start >= sentence.length - 1) {
        break;
      }

      // find the end index of the word.
      end = start + 1;
      while (end < sentence.length - 1 && sentence[end] != ' ') {
        ++end;
      }

      // let's reverse the word in-place.
      strRev(sentence, start, end - 1);
      start = end;
    }
  }
  static char[] getArray(String t) {
    char[] s = new char[t.length() + 1];
    int i = 0;
    for (; i < t.length(); ++i) {
      s[i] = t.charAt(i);
    }
    return s;
  }

  public static void main(String[] args) {
    char[] s = getArray("Hello World!");
    System.out.println(s);
    reverseWords(s);
    System.out.println(s);
  }
}
```

- Runtime complexity :

The runtime complexity of this solution is linear, O(n). Position of all the elements in the sentence is changed.

- Memory complexity :

The memory complexity of this solution is constant, O(1).

```
The solution reverses every word in-place i.e., it does not require any extra space.
```

### Remove Duplicates from a String
<hr>

Remove duplicate characters from a string which is passed by reference.

- Description :

Given a string that contains duplicate occurrences of characters, remove the duplicate occurrences.
```
The string is passed by reference. So you don’t need to return anything.
```
**Solution**

In this solution, we’ll keep two pointers or indices one for the current reading position and one for the current writing position. Whenever we encounter the first occurrence of a character, we add it to the HashSet. Any character already existing in the HashSet is skipped on any subsequent occurrence. Below is an overview of the algorithm:
```
read_pos = 0
write_pos = 0

for each character 'c' in str
  if 'c' not found in hashset
    add 'c' to hashset
    str[write_pos] = str[read_pos]
    write_pos++
  read_pos++
```
- Code :tada:
```java
class RemoveDuplicates {
  // this solution uses extra memory
  // to keep all characters present in string.

  static void removeDuplicates(char[] str) {
    Set<Character> hashset = new LinkedHashSet<Character> ();

    int writeIndex = 0;
    int readIndex = 0;

    while (readIndex != str.length) {

      if (!hashset.contains(str[readIndex])) {

        hashset.add(str[readIndex]);
        str[writeIndex] = str[readIndex];
        ++writeIndex;
      }

      ++readIndex;
    }

    str[writeIndex] = '\0';
  }

  // Test Program

  static char[] getArray(String t) {
    char[] s = new char[t.length() + 1];
    int i = 0;
    for (; i < t.length(); ++i) {
      s[i] = t.charAt(i);
    }
    s[i] = '\0';
    return s;
  }

  static void print(char[] s) {
    int i = 0;
    while (s[i] != '\0') {
      System.out.print(s[i]);
      ++i;
    }
    System.out.println();
  }

  public static void main(String[] args) {
  
    char[] input = getArray("dabbac");
    System.out.print("Before: ");
    System.out.println(input);
    RemoveDuplicates.removeDuplicates(input);
    System.out.print("After: ");
    print(input);
  }
}
```

- Runtime complexity :

The runtime complexity of this solution is linear, O(n).

- Memory complexity :

The memory complexity of this solution is linear, O(n).

**Solution 2**

This algorithm does not require any extra memory. It maintains two pointers indices: one for the read position and one for the write position. For every character in the input string that is present in the sub-string `[0, write_pos]`, we skip it; otherwise, we write the character at `read_pos to write_pos`. Here is the algorithm:

```
read_pos = 0
write_pos = 0
while read_pos less than length(str)
  if str[read_pos] not found in sub_string(0, write_pos)
    str[write_pos] = str[read_pos]
    ++write_pos
  ++read_pos
```

- Code :tada:
```java
class RemoveDuplicates {
  // this solution does not require any extra memory
  // but runs in O(n^2) time

  static void removeDuplicates(char[] str) {
    if (str == null || str.length == 0) {
      return;
    }

    int writeIndex = 0;
    for (int i = 0; i < str.length; i++) {
      boolean found = false;

      for (int j = 0; j < writeIndex; j++) {
        if (str[i] == str[j]) {
          found = true;
          break;
        }
      }

      if (!found) {
        str[writeIndex] = str[i];
        writeIndex++;
      }
    }

    if (writeIndex != str.length) {
      str[writeIndex] = '\0';
    }
  }

  /// Test Program.
  static void print(char[] s) {
    int i = 0;
    while (s[i] != '\0') {
      System.out.print(s[i]);
      ++i;
    }
    System.out.println();
  }

  static char[] getArray(String t) {
    char[] s = new char[t.length() + 1];
    int i = 0;
    for (; i < t.length(); ++i) {
      s[i] = t.charAt(i);
    }
   
    return s;
  }
  
  public static void main(String[] args) {
    char[] input = getArray("dabbac");
    System.out.print("Before: ");
    System.out.println(input);
    RemoveDuplicates.removeDuplicates(input);
    System.out.print("After: ");
    print(input);
  }
}
```
- Runtime complexity :

The runtime complexity of this solution is quadratic, O(n^2).

- Memory complexity :

The memory complexity of this solution is constant, O(1).

### Remove White Spaces from a String
<hr>
Given a null terminated string, remove any white spaces (tabs or spaces).

- Description :

Given a null terminated string, remove any white spaces (tabs or spaces). For example:

All greek to me. After removing the white spaces, the string should look like this:
Allgreektome.

- Solution :

This problem can be solved with two pointers. Here is an overview:
```
read_ptr and write_ptr initialized to start of string, str[0]

With the read_ptr, iterate over the input string reading one character at a time.
While moving read_ptr towards the end of the array:
  if read_ptr points to a white space, skip
  if read_ptr points to any other character, write that to write_ptr and increment the write_ptr.

Terminate the loop when the read_ptr reaches the end of the string.
At this point, the write_ptr will point to the string with all white spaces removed.
```
- Code :tada:
```java
class RemoveSpaces {
  static boolean isWhiteChar(char c) {
    // there can be more white space characters
    // but for simplicity lets assume that we have
    // only two white space character
    // i.e. space and tab
    if (c == ' ' || c == '\t') {
      return true;
    }
    return false;
  }

  static void removeWhiteSpaces(char[] s) {
    if (s == null || s.length == 0 || s[0] == '\0') {
      return;
    }

    // We will use read, write pointers here.
    // Write pointer will follow the read pointer
    // and only write characters read that are neither
    // a space (' ') nor a tab ('\t').

    int readPtr = 0;
    int writePtr = 0;
    while (readPtr < s.length) {
      // Lets assume there are only two white
      // space characters: space and tab.
      if (!isWhiteChar(s[readPtr])) {
        s[writePtr] = s[readPtr];
        ++writePtr;
      }
      ++readPtr;
    }

    // Let's mark the end of string.
    s[writePtr] = '\0';
  }

  static void print(char[] s) {
    int i = 0;
    while (i < s.length && s[i] != '\0') {
      System.out.print(s[i]);
      ++i;
    }
    System.out.println();
  }

  static char[] getArray(String t) {
    char[] s = new char[t.length()];
    int i = 0;
    for (; i < t.length(); ++i) {
      s[i] = t.charAt(i);
    }
    return s;
  }

  public static void main(String[] args) {
    char[] s = getArray("All greek to me");
    System.out.print("Before: ");
    print(s);
    removeWhiteSpaces(s);
    System.out.print("After: ");
    print(s);
  }
}
```
- Runtime complexity :

The runtime complexity of this solution is linear, O(n).

- Memory complexity :

The memory complexity of this solution is linear, O(1).

### Word Break Problem
<hr>

Given a dictionary of words and an input string tell whether the input string can be completely segmented into dictionary words.

- Description :

We are given a dictionary of words and a large input string. We have to find out whether the input string can be completely segmented into the words of a given dictionary. The following two examples elaborate on the problem further.

- Solution :

We can solve this problem by segmenting the large string at each possible position to see if the string can be completely segmented to words in the dictionary. If we write the algorithm in steps it will be as follows:
```
n = length of input string
for i = 0 to n - 1
  first_word = substring (input string from index [0, i] )
  second_word = substring (input string from index [i + 1, n - 1] )
  if dictionary has first_word
    if second_word is in dictionary OR second_word is of zero length, then return true
    recursively call this method with second_word as input and return true if it can be segmented
The algorithm will compute two strings from scratch in each iteration of the loop. Worst case scenario, there would be a recursive call of the second_word each time. This shoots the time complexity up to 2^n.
```
Code :tada:
```java

class StringSegmentation {

  public static boolean canSegmentString(String s, Set <String> dictionary) {
    for (int i = 1; i <= s.length(); ++i) {
      String first = s.substring(0, i);
      if (dictionary.contains(first)) {
        String second = s.substring(i);

        if (second == null || second.length() == 0 || dictionary.contains(second) || canSegmentString(second, dictionary)) {
          return true;
        }

      }
    }
    return false;
  }

  public static void main(String[] args) {
    Set < String > dictionary = new HashSet < String > ();
    String s = new String();
    s = "hellonow";

    dictionary.add("hello");
    dictionary.add("hell");
    dictionary.add("on");
    dictionary.add("now");
    if (canSegmentString(s, dictionary)) {
      System.out.println("String Can be Segmented");
    } else {
      System.out.println("String Can NOT be Segmented");
    }
  }
}
```
You can see that we may be computing the same substring multiple times, even if it doesn’t exist in the dictionary. This redundancy can be fixed by memoization, where we remember which substrings have already been solved To achieve memoization, we can store the second string in a new set each time.This will reduce both time and memory complexities.

- Runtime complexity :

The runtime complexity of this solution is exponential, O(2^n), if we use only recursion.

With memoization, the runtime complexity of this solution can be improved to be polynomial, O(n^2).

- Memory complexity :

The memory complexity of this solution is polynomial, O(n^2).
```
Memory Complexity is O(n^2), because we create a substring on each recursion call. Creating a substring can be avoided if we pass indices.
```

### Find all Palindrome Substrings
<hr>

Given a string, find all substrings that are palindromes.

- Description :

Given a string find all non-single letter substrings that are palindromes.

**Solution**

You can see that we may be computing the same substring multiple times, even if it doesn’t exist in the dictionary. This redundancy can be fixed by memoization, where we remember which substrings have already been solved To achieve memoization, we can store the `second` string in a new set each time.This will reduce both time and memory complexities. A palindrome is a word, phrase, number, or other sequence of characters which reads the same backwards as it reads forwards. A naive solution of this problem is to find all substrings of a given string and check whether each substring is a palindrome or not. This solution has a complexity of O(n^3).

- Code :tada:
```java
class PalindromeSubStrings{
  public static boolean isPalindrome(String input, int i, int j) {
    while(j > i){
      if(input.charAt(i) != input.charAt(j))
        return false;
      i++;
      j--;
    }
    return true;
  }

  public static int findAllPalindromeSubstrings(String input) {
    int count = 0;
    for(int i = 0 ; i < input.length() ; i++) {
      for(int j = i + 1 ; j < input.length() ; j++) {
        if(isPalindrome(input,i,j)){
          System.out.println(input.substring(i,j+1));
          count++;
        }
      }
    }
  
    return count;
  }
  public static void main(String[] args) {
    String str = "aabbbaa";
    int count = findAllPalindromeSubstrings(str);
    System.out.println("Total palindrome substrings: " + count);
  }
}
```
- Runtime complexity- :

The runtime complexity of this solution is polynomial, O(n^3).

- Memory complexity :

The memory complexity of this solution is constant, O(1).

**Solution 2**

We can reduce the runtime complexity of this algorithm to O(n^2) from O(n^3) by using the following approach. For each letter in the input string, start expanding to the left and right while checking for even and odd length palindromes. Move to the next letter if we know a palindrome doesn’t exist. We expand one character to the left and right and compare them. If both of them are equal, we print out the palindrome substring.

- Code :tada:
```java
class PalindromeSubStrings{
  public static int findPalindromesInSubString(String input, int j, int k) {
    int count = 0;
    for (; j >= 0 && k < input.length(); --j, ++k) {
      if (input.charAt(j) != input.charAt(k)) {      
        break;
      } 
      System.out.println(input.substring(j, k+1));
      count++;
    }
    return count;
  }

  public static int findAllPalindromeSubstrings(String input) {
    int count = 0;
    for(int i = 0 ; i < input.length() ; ++i) {
      count+= findPalindromesInSubString(input, i-1, i+1);
      count+= findPalindromesInSubString(input, i, i+1);
    }

    return count;
  }

  public static void main(String[] args) {
    String str = "aabbbaa";
    int count = findAllPalindromeSubstrings(str);
    System.out.println("Total palindrome substrings: " + count);
  }
}  
```
- Runtime complexity :

The runtime complexity of this solution is polynomial, O(n^2).

- Memory complexity :

The memory complexity of this solution is constant, O(1).

### Balanced Parentheses
<hr>

- Problem Statement :

For a given number ‘N’, write a function to generate all combination of ‘N’ pairs of balanced parentheses.

- Example 1 :
```
Input: N=2 Output: (()), ()()
```
- Example 2 :
```
Input: N=3 Output: ((())), (()()), (())(), ()(()), ()()()
```
- Basic Solution :
  
This problem follows the Subsets pattern and can be mapped to Permutations. We can follow a similar BFS approach. Let’s take Example-2 mentioned above to generate all the combinations of balanced parentheses. Following a BFS approach, we will keep adding open parentheses ( or close parentheses ). At each step we need to keep two things in mind:

We can’t add more than ‘N’ open parenthesis.
To keep the parentheses balanced, we can add a close parenthesis ) only when we have already added enough open parenthesis (. For this, we can keep a count of open and close parenthesis with every combination.
Following this guideline, let’s generate parentheses for N=3:

Start with an empty combination: “”
At every step, let’s take all combinations of the previous step and add ( or ) keeping the above-mentioned two rules in mind.
For the empty combination, we can add ( since the count of open parenthesis will be less than ‘N’. We can’t add ) as we don’t have an equivalent open parenthesis, so our list of combinations will now be: “(”
For the next iteration, let’s take all combinations of the previous set. For “(” we can add another ( to it since the count of open parenthesis will be less than ‘N’. We can also add ) as we do have an equivalent open parenthesis, so our list of combinations will be: “((”, “()”
In the next iteration, for the first combination “((”, we can add another ( to it as the count of open parenthesis will be less than ‘N’, we can also add ) as we do have an equivalent open parenthesis. This gives us two new combinations: “(((” and “(()”. For the second combination “()”, we can add another ( to it since the count of open parenthesis will be less than ‘N’. We can’t add ) as we don’t have an equivalent open parenthesis, so our list of combinations will be: “(((”, “(()”, ()("
Following the same approach, next we will get the following list of combinations: “((()”, “(()(”, “(())”, “()((”, “()()”
Next we will get: “((())”, “(()()”, “(())(”, “()(()”, “()()(”
Finally, we will have the following combinations of balanced parentheses: “((()))”, “(()())”, “(())()”, “()(())”, “()()()”
We can’t add more parentheses to any of the combinations, so we stop here.

Code :tada:
```java

import java.util.*;

class ParenthesesString {
  String str;
  int openCount; // open parentheses count
  int closeCount; // close parentheses count

  public ParenthesesString(String s, int openCount, int closeCount) {
    str = s;
    this.openCount = openCount;
    this.closeCount = closeCount;
  }
}

class GenerateParentheses {

  public static List<String> generateValidParentheses(int num) {
    List<String> result = new ArrayList<String>();
    Queue<ParenthesesString> queue = new LinkedList<>();
    queue.add(new ParenthesesString("", 0, 0));
    while (!queue.isEmpty()) {
      ParenthesesString ps = queue.poll();
      // if we've reached the maximum number of open and close parentheses, add to the result
      if (ps.openCount == num && ps.closeCount == num) {
        result.add(ps.str);
      } else {
        if (ps.openCount < num) // if we can add an open parentheses, add it
          queue.add(new ParenthesesString(ps.str + "(", ps.openCount + 1, ps.closeCount));

        if (ps.openCount > ps.closeCount) // if we can add a close parentheses, add it
          queue.add(new ParenthesesString(ps.str + ")", ps.openCount, ps.closeCount + 1));
      }
    }
    return result;
  }

  public static void main(String[] args) {
    List<String> result = GenerateParentheses.generateValidParentheses(2);
    System.out.println("All combinations of balanced parentheses are: " + result);

    result = GenerateParentheses.generateValidParentheses(3);
    System.out.println("All combinations of balanced parentheses are: " + result);
  }
}
```
Let’s try to estimate how many combinations we can have for ‘N’ pairs of balanced parentheses. If we don’t care for the ordering - that ) can only come after ( - then we have two options for every position, i.e., either put open parentheses or close parentheses. This means we can have a maximum of 2^N​ combinations. Because of the ordering, the actual number will be less than 2^N​

- Time complexity :

You will realize that, in the worst case, it is equivalent to a binary tree, where each node will have two children. This means that we will have 2^N leaf nodes and 2^N-1 intermediate nodes. So the total number of elements pushed to the queue will be 2^N + 2^N −1, which is asymptotically equivalent to O(2^N). While processing each element, we do need to concatenate the current string with ( or ). This operation will take O(N), so the overall time complexity of our algorithm will be O(N2^N)*. This is not completely accurate but reasonable enough to be presented in the interview.

The actual time complexity (O(4^n/sqrt{n}) is bounded by the Catalan number and is beyond the scope of a coding interview.

- Space complexity :

All the additional space used by our algorithm is for the output list. Since we can’t have more than O(2^N) combinations, the space complexity of our algorithm is O(N2^N)*.

- Recursive Solution :

Here is the recursive algorithm following a similar approach:

```java
import java.util.*;

class GenerateParenthesesRecursive {

  public static List<String> generateValidParentheses(int num) {
    List<String> result = new ArrayList<String>();
    char[] parenthesesString = new char[2 * num];
    generateValidParenthesesRecursive(num, 0, 0, parenthesesString, 0, result);
    return result;
  }

  private static void generateValidParenthesesRecursive(int num, int openCount, int closeCount,
      char[] parenthesesString, int index, List<String> result) {

    // if we've reached the maximum number of open and close parentheses, add to the result
    if (openCount == num && closeCount == num) {
      result.add(new String(parenthesesString));
    } else {
      if (openCount < num) { // if we can add an open parentheses, add it
        parenthesesString[index] = '(';
        generateValidParenthesesRecursive(num, openCount + 1, closeCount, parenthesesString, index + 1, result);
      }

      if (openCount > closeCount) { // if we can add a close parentheses, add it
        parenthesesString[index] = ')';
        generateValidParenthesesRecursive(num, openCount, closeCount + 1, parenthesesString, index + 1, result);
      }
    }
  }

  public static void main(String[] args) {
    List<String> result = GenerateParenthesesRecursive.generateValidParentheses(2);
    System.out.println("All combinations of balanced parentheses are: " + result);

    result = GenerateParenthesesRecursive.generateValidParentheses(3);
    System.out.println("All combinations of balanced parentheses are: " + result);
  }
}
```

### Longest Substring with Distinct Characters
<hr>

Given a string, find the length of the longest substring, which has all distinct characters.

- Example 1 :
```
Input: String="aabccbb" Output: 3 Explanation: The longest substring with distinct characters is "abc".
```
- Example 2 :
```
Input: String="abbbb" Output: 2 Explanation: The longest substring with distinct characters is "ab".
```
**Solution**
This problem follows the Sliding Window pattern, and we can use a similar dynamic sliding window strategy as discussed in Longest Substring with K Distinct Characters. We can use a HashMap to remember the last index of each character we have processed. Whenever we get a duplicate character, we will shrink our sliding window to ensure that we always have distinct characters in the sliding window.

Code :tada:
```java

import java.util.*;

class NoRepeatSubstring {
  public static int findLength(String str) {
    int windowStart = 0, maxLength = 0;
    Map<Character, Integer> charIndexMap = new HashMap<>();
    // try to extend the range [windowStart, windowEnd]
    for (int windowEnd = 0; windowEnd < str.length(); windowEnd++) {
      char rightChar = str.charAt(windowEnd);
      // if the map already contains the 'rightChar', shrink the window from the beginning so that
      // we have only one occurrence of 'rightChar'
      if (charIndexMap.containsKey(rightChar)) {
        // this is tricky; in the current window, we will not have any 'rightChar' after its previous index
        // and if 'windowStart' is already ahead of the last index of 'rightChar', we'll keep 'windowStart'
        windowStart = Math.max(windowStart, charIndexMap.get(rightChar) + 1);
      }
      charIndexMap.put(rightChar, windowEnd); // insert the 'rightChar' into the map
      maxLength = Math.max(maxLength, windowEnd - windowStart + 1); // remember the maximum length so far
    }

    return maxLength;
  }

  public static void main(String[] args) {
    System.out.println("Length of the longest substring: " + NoRepeatSubstring.findLength("aabccbb"));
    System.out.println("Length of the longest substring: " + NoRepeatSubstring.findLength("abbbb"));
    System.out.println("Length of the longest substring: " + NoRepeatSubstring.findLength("abccde"));
  }
}
```
- Time Complexity :

The above algorithm’s time complexity will be O(N), where ‘N’ is the number of characters in the input string.

- Space Complexity :

The algorithm’s space complexity will be O(K)O(K), where KK is the number of distinct characters in the input string. This also means K<=NK<=N, because in the worst case, the whole string might not have any duplicate character, so the entire string will be added to the HashMap. Having said that, since we can expect a fixed set of characters in the input string (e.g., 26 for English letters), we can say that the algorithm runs in fixed space O(1)O(1); in this case, we can use a fixed-size array instead of the HashMap.

## Linked List

### Introduction TO Linked Lists
<hr>

A linked list is a linear data structure consisting of nodes where each node contains data and a pointer to the next node in the list. There are two kinds of linked lists:

```
Singly linked list 
Doubly link
```
- Singly Linked List :

A singly linked list can only be traversed in one direction, meaning, from the first node (head) towards the last node. The last node points to NULL, indicating the end of the list.

- Pros :

Insertion and deletion at head is more efficient compared to the corresponding operations in an array.
Changes are localized when inserting and deleting somewhere in the middle of the linked list. In the case of an array, all subsequent elements need to be moved around. Of course, if you first have to search for the position to insert or delete in a linked list, then it still takes O(n) in the worst case.
- Cons :

As each node also contains a pointer, it has a memory overhead.
We cannot access a node through indexing directly, rather we have to traverse from the start to access an element at a given position n.
Reverse traversing is not possible with a singly linked list.

- Doubly Linked List :

Each node in a doubly linked list contains a pointer to the next node as well as pointer to the previous node. This allows the list to be traversed in both directions: forward and backward.

Doubly linked lists have all the advantages of singly-linked lists while providing some additional pros and cons.

- Pros :

Insert and delete at the head as well as tail are O(1) operations
The list can be traversed forward as well as backward

- Cons :

Have greater space overhead than singly-linked lists

- Singly vs. Doubly linked list table :

Deletion at the tail is one of the operations that distinguishes a doubly-linked list from a singly-linked list. The following table shows a side by side comparison of key operations on both.

| Operations | Singly Linked List | Doubly Linked List|
| --- | --- | --- |
| Insert at head | O(1) | O(1) |
| Delete at head | O(1)	| O(1) |
| Insert at tail | O(n)	| O(1) |
| Delete at tail | O(n)	| O(1) |

In terms of space, if there are `n` nodes in a linked list, `d` is the (average) number of bytes of data in each node and `p` is the number of bytes consumed by a pointer, then a `singly linked list` consumes n*(d+p) bytes, whereas a `doubly linked list` consumes n*(d+2p) bytes.

### Insertion in a Singly Linked List (insert at End)
<hr>

- Introduction :

Now, we are going to explain the second part (Insertion at End) and look at its examples, along with one coding challenge for the sake of practice. So let’s see how elements are inserted at the end of a linked list. In this type of insertion, we add an element at the end of the list.

- Problem Statement :

In the code snippet provided below, you will complete the void insertAtEnd(T data) method. This will take a generic type T value called data and insert that value at the end of the list. This code would be the part of the SinglyLinkedList class that we created in the previous lesson, therefore, any private members of that class can be accessed inside the function as well. After writing the code, run it and see how many tests you passed.

- Method Prototype :
```
void insertAtEnd(T data)
```
- Output :

The return type of the method is `void`. The object on which it is called will be modified only.

- Sample Input :

```
linkedlist = 0->1->2 data = 3
```
- Sample Output :

```
linkedlist = 0->1->2->3
```
**Solution**

If you grasped the logic behind insertion at the head of a linked list, this shouldn’t be much of a challenge. If the list is empty, the situation is exactly like insertion at the head. Otherwise, we can use a loop to reach the tail of the list and set our new node as the `nextNode` of the `last` node.

- Code :tada:
```java

public class SinglyLinkedList<T> {
//Node inner class for SLL
    public class Node {
        public T data;
        public Node nextNode;

    }

    public Node headNode; //head node of the linked list
    public int size;      //size of the linked list

    //Constructor - initializes headNode and size
    public SinglyLinkedList() {
        headNode = null;
        size = 0;
    }

    //Helper Function that checks if List is empty or not 
    public boolean isEmpty() {
        if (headNode == null) return true;
        return false;
    }

    //Inserts new data at the start of the linked list
    public void insertAtHead(T data) {
        //Creating a new node and assigning it the new data value
        Node newNode = new Node();
        newNode.data = data;
        //Linking head to the newNode's nextNode
        newNode.nextNode = headNode;
        headNode = newNode;
        size++;
    }

    // Helper Function to printList
    public void printList() {
        if (isEmpty()) {
            System.out.println("List is Empty!");
            return;
        }

        Node temp = headNode;
        System.out.print("List : ");
        while (temp.nextNode != null) {
            System.out.print(temp.data.toString() + " -> ");
            temp = temp.nextNode;
        }
        System.out.println(temp.data.toString() + " -> null");
    }
    
    //Inserts new data at the end of the linked list
    public void insertAtEnd(T data) {
        //if the list is empty then call insertATHead()
        if (isEmpty()) {
            insertAtHead(data);
            return;
        }
        //Creating a new Node with value data 
        Node newNode = new Node();
        newNode.data = data;
        newNode.nextNode = null;

        Node last = headNode;
        //iterate to the last element 
        while (last.nextNode != null) {
            last = last.nextNode;
        }
        //make newNode the next element of the last node
        last.nextNode = newNode;
        size++;
    }
}
```
- Time Complexity :

This algorithm traverses the entire linked list, and hence, works in O(n) time.

### Search in Singly Linked List
<hr>

- Introduction :

Now, we will take a look at the second most important operation, i.e. searching for an element in a linked list. This exercise of finding a value in a Singly Linked List is relatively more straightforward than the other three operations of insertion.

The steps to search for a node in a Singly Linked List are as follows:

Start from the `headNode`.
Traverse the list till you either find a node with the given value, or you reach the end showing that the node being searched doesn’t exist.

- Problem Statement :

If you know how to insert an element in a list, then searching for an item will not be that difficult for you. Now, based on the steps mentioned above, we have designed a simple coding exercise for your practice. There is a solution placed in the solution section for your help, but try to solve it on your own first.

- Method Prototype :
```
boolean searchNode(T data)
```
- Output :

It returns true or false to show if a certain value does or does not exists in the list.

- Sample Input :
```
linkedlist = 5->90->10->4 and value = 4
```
- Sample Output :
```
true
```
**Soution**

In this function, we traverse through the list, checking whether the currentNode’s `data` matches the searched value `data`. If the currentNode’s `data` matches the searched value `data`, we will return `True` else we will return `False`.

- Code :tada:
```java
public class SinglyLinkedList<T> {
    //Node inner class for SLL
    public class Node {
        public T data;
        public Node nextNode;

    }

    //head node of the linked list
    public Node headNode;
    public int size;

    //constructor
    public SinglyLinkedList() {
        headNode = null;
        size = 0;
    }

    public boolean isEmpty() {

        if (headNode == null) return true;
        return false;
    }

    //Inserts new data at the start of the linked list
    public void insertAtHead(T data) {
        //Creating a new node and assigning it the new data value
        Node newNode = new Node();
        newNode.data = data;
        //Linking head to the newNode's nextNode
        newNode.nextNode = headNode;
        headNode = newNode;
        size++;
    }

    //Inserts new data at the end of the linked list
    public void insertAtEnd(T data) {
        //if the list is empty then call insertATHead()
        if (isEmpty()) {
            insertAtHead(data);
            return;
        }
        //Creating a new Node with value data
        Node newNode = new Node();
        newNode.data = data;
        newNode.nextNode = null;

        Node last = headNode;
        //iterate to the last element
        while (last.nextNode != null) {
            last = last.nextNode;
        }
        //make newNode the next element of the last node
        last.nextNode = newNode;
        size++;
    }

    //inserts data after the given prev data node
    public void insertAfter(T data, T previous) {

        //Creating a new Node with value data
        Node newNode = new Node();
        newNode.data = data;
        //Start from head node
        Node currentNode = this.headNode;
        //traverse the list until node having data equal to previous is found
        while (currentNode != null && currentNode.data != previous) {
            currentNode = currentNode.nextNode;
        }
        //if such a node was found
        //then point our newNode to currentNode's nextElement
        if (currentNode != null) {
            newNode.nextNode = currentNode.nextNode;
            currentNode.nextNode = newNode;
            size++;
        }
    }

    public void printList() {
        if (isEmpty()) {
            System.out.println("List is Empty!");
            return;
        }

        Node temp = headNode;
        System.out.print("List : ");

        while (temp.nextNode != null) {
            System.out.print(temp.data.toString() + " -> ");
            temp = temp.nextNode;
        }

        System.out.println(temp.data.toString() + " -> null");
    }

    //Searches a value in the given list.
    public boolean searchNode(T data) {
        //Start from first element
        Node currentNode = this.headNode;

        //Traverse the list till you reach end
        while (currentNode != null) {
            if (currentNode.data.equals(data))
                return true; //value found

            currentNode = currentNode.nextNode;
        }
        return false; //value not found
    }
}

```
- Time Complexity :

The time complexity for this algorithm is O(n) because we have to traverse through the list.

### Deletion in Singly Linked List (Delete by Value)
<hr>

- Introduction :

This operation deletes the required node, e.g., n, from any position in a Singly Linked List. This deletion follows the following steps:

It takes in the value that needs to be deleted from the list.
It traverses the list searching for that value.
Once the node (n) with the required value is found, it connects n's previous node to the nextNode of n.
It then removes n from the list.

- Problem Statement :

In the code snippet given below, you have to implement the void deleteByValue(T data) method. In this method, we will pass a particular value that we want to delete from the list. The node containing this value could be anywhere on the list. It is also possible that such a node may not exist at all. Therefore, we would have to traverse the whole list until we find the value which needs to be deleted. If the value doesn’t exist, we simply return control to the calling function.

```
Note: This function removes only the first occurrence of the value from the list.
```
- Method Prototype :
```
void deleteByValue(T data)
```
- Output :
```
A linked list with the element removed.
```
- Sample Input :
```
linkedlist = 3->2->1->0, data = 1
```
- Sample Output :
```
linkedlist = 3->2->0
```
- Solution :

While traversing through the linked list, there are three cases we can come across:

List is empty
One element in the list
More than one element in the list
If the list is empty, then we have nothing to do; just return the control to calling function. For a single element in the list, we’ll call `deleteAtHead()`, and this will delete the value at the head.

If there is more than one element in the list, then we simply start traversing from the `headNode` and keep on checking until that node found and delete it.

- Code :tada:
```java

  public class SinglyLinkedList<T> {
    //Node inner class for SLL
    public class Node {
        public T data;
        public Node nextNode;

    }

    //head node of the linked list
    public Node headNode;
    public int size;

    //constructor
    public SinglyLinkedList() {
        headNode = null;
        size = 0;
    }

    public boolean isEmpty() {

        if (headNode == null) return true;
        return false;
    }

    //Inserts new data at the start of the linked list
    public void insertAtHead(T data) {
        //Creating a new node and assigning it the new data value
        Node newNode = new Node();
        newNode.data = data;
        //Linking head to the newNode's nextNode
        newNode.nextNode = headNode;
        headNode = newNode;
        size++;
    }

    //Inserts new data at the end of the linked list
    public void insertAtEnd(T data) {
        //if the list is empty then call insertATHead()
        if (isEmpty()) {
            insertAtHead(data);
            return;
        }
        //Creating a new Node with value data
        Node newNode = new Node();
        newNode.data = data;
        newNode.nextNode = null;

        Node last = headNode;
        //iterate to the last element
        while (last.nextNode != null) {
            last = last.nextNode;
        }
        //make newNode the next element of the last node
        last.nextNode = newNode;
        size++;
    }

    //inserts data after the given prev data node
    public void insertAfter(T data, T previous) {

        //Creating a new Node with value data
        Node newNode = new Node();
        newNode.data = data;
        //Start from head node
        Node currentNode = this.headNode;
        //traverse the list until node having data equal to previous is found
        while (currentNode != null && currentNode.data != previous) {
            currentNode = currentNode.nextNode;
        }
        //if such a node was found
        //then point our newNode to currentNode's nextElement
        if (currentNode != null) {
            newNode.nextNode = currentNode.nextNode;
            currentNode.nextNode = newNode;
            size++;
        }
    }

    public void printList() {
        if (isEmpty()) {
            System.out.println("List is Empty!");
            return;
        }

        Node temp = headNode;
        System.out.print("List : ");

        while (temp.nextNode != null) {
            System.out.print(temp.data.toString() + " -> ");
            temp = temp.nextNode;
        }

        System.out.println(temp.data.toString() + " -> null");
    }

    //Searches a value in the given list.
    public boolean searchNode(T data) {
        //Start from first element
        Node currentNode = this.headNode;

        //Traverse the list till you reach end
        while (currentNode != null) {
            if (currentNode.data.equals(data))
                return true; //value found

            currentNode = currentNode.nextNode;
        }
        return false; //value not found
    }

    //Deletes data from the head of list
    public void deleteAtHead() {
        //if list is empty then simply return
        if (isEmpty())
            return;
        //make the nextNode of the headNode equal to new headNode
        headNode = headNode.nextNode;
        size--;
    }

    //Deletes data given from the linked list
    public void deleteByValue(T data) {
        //if empty then simply return
        if (isEmpty())
            return;

        //Start from head node
        Node currentNode = this.headNode;
        Node prevNode = null; //previous node starts from null

        if(currentNode.data.equals(data)) {
            //data is at head so delete from head
            deleteAtHead();
            return;
        }
        //traverse the list searching for the data to delete
        while (currentNode != null) {
            //node to delete is found
            if (data.equals(currentNode.data)){
                prevNode.nextNode = currentNode.nextNode;
                size--;
                return; 
            }
            prevNode = currentNode;
            currentNode = currentNode.nextNode;
        }
    }
}   
```

`deleteByValue():` It takes a value as a parameter. Additionally, it searches for a node in the Singly Linked List that has the given data value while keeping track of current and previous nodes. If not found, it means no such value exists in the list. If found, it performs a series of steps to delete this value. However, before jumping to those steps, look at some of the terminologies that we used in the function:

`currentNode` – node we are currently standing at
`prevNode` – element that comes before `currentNode`
`nextNode` – pointer to the next node of `currentNode`

Executing the single line of code,
```
prevNode.nextNode = currentNode.nextNode
```
links the prevNode to the nextNode. The current node’s link will be destroyed from the list, and the garbage collector will take care of the deletion automatically.

- Time Complexity :

In the worst case, you would have to traverse until the end of the list. This means the time complexity will be O(n).

### Linked Lists vs Arrays
<hr>

Let's put the two data structures against each other to find out which is more efficient.

- Memory Allocation :

The main difference between a linked list and an array is the way they are allocated memory. Arrays instantiate a whole block of memory, e.g., array[1000] gets space to store 1000 elements at the start even if it doesn’t contain any element yet. On the other hand, a linked list only instantiates the portion of memory it uses.

- Insertion and Deletion :

For lists and arrays, many differences can be observed in the way elements are inserted and deleted. In a linked list, insertion and deletion at head happen in a constant amount of time (O(1)), while arrays take O(n) time to insert or delete a value because you have to shift the array elements left or right after that operation.

- Searching :

In an array, it takes constant time to access an index. In a linked list, you have to iterate the list from the start until you find the node with the correct value.

The table given below will summarize the performance difference between linked lists and arrays.

| Operation | Linked List | Array |
| --- | --- | --- |
| Access | O(n) | O(1) |
| Insert (at head) | O(1) | O(n) |
| Delete (at head) | O(1) | O(n) |
| Insert (at tail) | O(n) | O(n) |
| Delete (at tail) | O(n) | O(n) |

As you can see, there is a trade-off between the facilities provided by both structures. You will understand more about the working of linked lists in the lessons that follow.

### Find the Length of a Linked List
<hr>

- Problem Statement :

In this problem, you have to implement the method `int length()`, which will count the number of nodes in a linked list. An illustration is also provided for your understanding.

- Method Prototype :
```
int length()
```
Output :

The length of the given linked list.

- Sample Input :
```
linkedlist = 0->1->2-3->4
```
- Sample Output :
```
length = 5
```
**Solution**

```java
class CheckLength {
  public static void main( String args[] ) {
        SinglyLinkedList<String> list = new SinglyLinkedList<String>();
        list.insertAtEnd("This");
        list.insertAtEnd("list");
        list.insertAtEnd("is");
        list.insertAtEnd("Generic");
        list.printList();
        System.out.println("Length : " + list.length());
    }
}
```

- Explanation :

The logic behind it is very similar to that of the `search` function. The trick is to iterate through the list and keep count of how many nodes you’ve visited. This count is held in a variable that is returned when the end of the list is reached.

- Time Complexity :

Since this is a linear algorithm, the time complexity will be O(n).

### Reverse a Linked List
<hr>

- Problem Statement :

In this problem, you have to implement the public static void reverse(SinglyLinkedList list) method, which will take a linked list as input and reverse its content. An illustration is also provided for your help to see how the linked list will look after passing it to your function.

- Method Prototype :
```
public static void reverse(SinglyLinkedList list)
```
- Output :

A Singly linked list with all its content stored in reverse order.

- Sample Input :
```
linkedlist = 10->9->4->4-6
```
- Sample Output :
```
linkedlist = 6->4->4->9->10
```

**Solution**
- Code :tada:

```java
public static void reverse(SinglyLinkedList list){
	SinglyLinkedList.Node previous = null; //To keep track of the previous element, will be used in swapping links
			SinglyLinkedList.Node current = list.headNode; //firstElement
			SinglyLinkedList.Node next = null;

			//While Traversing the list, swap links
			while (current != null) {
					next = current.nextNode;
					current.nextNode = previous;
					previous = current;
					current = next;
			}
			//Linking Head Node with the new First Element
			list.headNode = previous;
}
```

- Explanation :

The brain of this solution lies in the loop, which iterates through the list. For any `current` node, its link with the `previous` node is reverse and the next stores `next` node in the list:

Store the `current` node’s `nextNode` in `next`
Set `current` node’s `nextNode` to `previous` (reversal)
Make the `current` node the new `previous` so that it can be used for the next iteration
Use `next` to move on to the next node
In the end, we simply point the head to the last node in our loop.

- Time Complexity :

The algorithm runs in O(n) since the list is traversed once.

### Detect Loop in a Linked List
<hr>

- Problem Statement :

In this problem, you have to implement the public static boolean detectLoop(SinglyLinkedList list) method, which will take a Singly linked list as input and find if there is a loop present in the list. A loop in a linked list occurs if any node contains a reference to any previous node, then a loop will be formed. An illustration is also provided for your understanding.

- Method Prototype :
```
public static boolean detectLoop(SinglyLinkedList list)
```
- Output :

It returns true if a loop exists in the linked list; otherwise, false.

- Sample Input :
```
linkedlist = 7->14->21->7
```
- Sample Output :
```
true
```

**Solution**
- Code :tada:
  
```java
    public static boolean detectLoop(SinglyLinkedList list) {
        SinglyLinkedList.Node slow = list.headNode;
        SinglyLinkedList.Node fast = list.headNode;
        
        while(slow != null && fast != null && fast.nextNode != null)
        {
            slow = slow.nextNode;	//the slow pointer will jump 1 step
            fast = fast.nextNode.nextNode; //the fast pointer will jump 2 steps 
			// when the pointers become equal then there must be a loop
            if(slow == fast){
                return true;
            }
        }
        return false;
    }
```

- Explanation :

This is the most optimized method to find out the loop in the LinkedList. We start traversing the LinkedList using two pointers called slow and fast. Move slow by one (line # 9) and fast by two (line # 10). If these pointers meet at the same node, then there is a loop. If these pointers do not meet, then LinkedList doesn’t have a loop.

- Time Complexity :

The algorithm runs in Constant with O(n) with the Auxiliary Space complexity of O(1).

### Find the Middle Node of a Linked List
<hr>

- Problem Statement :

In this problem, you have to implement the public static Object findMiddle(SinglyLinkedList list) method, which will take a linked list as an input and return the value at the middle node of the list. An illustration is also provided for your understanding.

- Method Prototype :
```
public static Object findMiddle(SinglyLinkedList list)
```
- Output :

The value at the middle node in a linked list.

- Sample Input :
```
linkedlist = 7->14->10->21
```
- Sample Output :
```
mid = 14
```
**Solution**
- Code :tada;

```java
    public static  Object findMiddle(SinglyLinkedList list) {
        //if list is empty, then return null
        if (list.isEmpty())
            return null;
        
        //both nodes start from the head
        SinglyLinkedList.Node mid = list.headNode;
        SinglyLinkedList.Node current = list.headNode;
        
        while(mid != null && current != null && current.nextNode != null)
        {
            //current jumps 2 nodes on each iteration
            current = current.nextNode.nextNode;
            //if current is not null (end of list is not reached)
            if(current != null){
                //then mid jumps 1 node
                //mid is always halfway behind current
                mid = mid.nextNode;
            }
        }
        return mid.data;
    }
```

- Explanation :

We are using two pointers, which will work simultaneously. Think of it this way:

The `current` pointer moves two steps at a time till the end of the list
The `mid` pointer moves one step at a time
When the `current` pointer reaches the end, the `mid` pointer will be at the middle

- Time Complexity :

We are traversing the linked list at twice the speed, so it is certainly faster. However, the bottleneck complexity is still O(n).

### Remove Duplicates from a Linked List
<hr>

- Problem Statement :

In this problem, you have to implement `public static void removeDuplicates(SinglyLinkedList list)` method. This method will take a Singly linked list as input and remove all the elements that appear more than once in the list. An illustration is also provided for your understanding.

- Method Prototype :
```
public static void removeDuplicates(SinglyLinkedList list)
```
- Output :

The linked list with all the duplicates removed.

- Sample Input :
```
linkedlist = 7->14->21->14->22->null
```
- Sample Output :
```
linkedlist = 7->14->21->22->null
```
- Solution**
- Code :tada:

```java
    public static void removeDuplicates(SinglyLinkedList list) {
        SinglyLinkedList.Node current = list.headNode; // will be used for outer loop
        SinglyLinkedList.Node compare = null;     // will be used for inner loop

        while (current != null && current.nextNode != null) {
            compare = current;
            while (compare.nextNode != null) {
                if (current.data.equals(compare.nextNode.data)) { //check if duplicate
                    compare.nextNode = compare.nextNode.nextNode;
                } else {
                    compare = compare.nextNode;
                }
            }
            current = current.nextNode;
        }
    }
 ```
    
- Explanation :

This solution is simply a brute force solution. In this solution, we traverse the linked list using two loops. The pointer `current` keeps track of the outer loop, and the pointer `compare` is used for the inner loop. When both of these pointers point to the same value, then that node is deleted. This is not the most efficient approach to solve this problem. It can also be solved using a Hash Table.

- Time Complexity :

This algorithm has two nested loops. Hence, the time complexity is O(n^2).

```
Note: The solution provided above is not the optimal solution for this problem. A more efficient approach is to use hashing instead.
```

### Return the Nth node from End
<hr>

- Problem Statement :

In this problem, you have to implement `Object nthElementFromEnd(SinglyLinkedList list, int n)` method, which will take a linked list as an input and returns the nth element of the list from the end. To solve this, you will have to come up with a formula by comparing multiple outputs and inputs and identifying a common pattern. An illustration is also provided for your understanding.

- Method Prototype :
```
public static Object nthElementFromEnd(SinglyLinkedList list, int n)
```
- Output: 

It will return nth node from the end of the linked list.

- Sample Input :
```
linkedlist = 22->18->60->78->47->39->99 and n=3
```
- Sample Output :
```
47
```
**Solution**
- Code :tada:
```java

    public static Object nthElementFromEnd(SinglyLinkedList list, int n) {
        int size = list.getSize();
        n = size - n + 1; //we can use the size variable to calculate distance from start
        if (size == 0 || n > size) {
            return null; //returns null if list is empty or n is greater than size
        }
        SinglyLinkedList.Node current = list.getHeadNode();
        int count = 1;
        //traverse until count is not equal to n
        while (current != null) {
            if (count == n)
                return current.data;
            count++;
            current = current.nextNode;
        }
        return null;
    }
```
- Explanation :

In the above solution, we first use the getter function `list.getSize()` to access the length of the list. Then we find the node which is at x position from the start.

- Time Complexity :

In the worst-case time complexity of this algorithm is O(n). Because we might have to access the 1st element from the end.

### Implementation of Linked List
<hr>

Linked list implementation will be covered in this lesson. We'll use this implementation in the whole chapter. Before moving on to the challenges of the linked list, let’s look at the implementation of `LinkedListNode` and `LinkedList` classes first. These classes are prepended in all the coming challenges of the chapter.

- Implementation of LinkedListNode Class :
- Code :tada:
```java
class LinkedListNode {
    public int key;
    public int data;
    public LinkedListNode next;
    public LinkedListNode arbitraryPointer;

    public LinkedListNode(int data) {
        this.data = data;
        this.next = null;
    }

    public LinkedListNode(int key, int data) {
        this.key = key;
        this.data = data;
        this.next = null;
    }

    public LinkedListNode(int data, LinkedListNode next) {
        this.data = data;
        this.next = next;
    }

    public LinkedListNode(int data, LinkedListNode next, LinkedListNode arbitraryPointer) {
        this.data = data;
        this.next = next;
        this.arbitraryPointer = arbitraryPointer;
    }
}
Implementation of LinkedList Class
import java.util.*;

class LinkedList { 

    public static LinkedListNode insertAtHead(LinkedListNode head, int data) {
        LinkedListNode newNode = new LinkedListNode(data);
        newNode.next = head;
        return newNode;
    }

    public static LinkedListNode insertAtTail(LinkedListNode head, int data) {
        LinkedListNode newNode = new LinkedListNode(data);
        if (head == null) {
            return newNode;
        }
        LinkedListNode temp = head;
        while (temp.next != null) {
            temp = temp.next;
        }
        temp.next = newNode;
        return head;
    }

    public static LinkedListNode createLinkedList(ArrayList<Integer> lst) {
        LinkedListNode head = null;
        LinkedListNode tail = null;
        for (Integer x : lst) {
            LinkedListNode newNode = new LinkedListNode(x);
            if (head == null) {
                head = newNode;
            } else {
                tail.next = newNode;
            }
            tail = newNode;
        }
        return head;
    }

    public static LinkedListNode createLinkedList(int[] arr) {
        LinkedListNode head = null;
        LinkedListNode tail = null;
        for (int i = 0; i < arr.length; ++i) {
            LinkedListNode newNode = new LinkedListNode(arr[i]);
            if (head == null) {
                head = newNode;
            } else {
                tail.next = newNode;
            }
            tail = newNode;
        }
        return head;
    }

    public static LinkedListNode createRandomList(int length) {
        LinkedListNode listHead = null;
        Random generator = new Random();
        for(int i = 0; i < length; ++i) {
            listHead = insertAtHead(listHead, generator.nextInt(100));
        }
        return listHead;
    }

    public static void display(LinkedListNode head) {
        LinkedListNode temp = head;
        while (temp != null) {
            System.out.printf("%d", temp.data);
            temp = temp.next;
            if (temp != null) {
              System.out.printf(", ");
            }
        }
        System.out.println();
    }  
}

class Pair<X, Y> {
    public X first;
    public Y second;
    public Pair(X first, Y second) {
    this.first = first;
    this.second = second;
  }
}
```

### Intersection Point of Two Lists
<hr>

Given the head nodes of two linked lists that may or may not intersect, find out if they intersect and return the point of intersection. Return null otherwise.

- Description :

Given the head nodes of two linked lists that may or may not intersect, find out if they do in fact intersect and return the point of intersection. Return null otherwise

- Hints :
Find the length of both linked lists.

The linked lists have to physically intersect. This means that their addresses need to be the same. If two nodes have the same data but their addresses are not the same, the lists won’t intersect and the function should return NULL.

**Solution**

The first solution that comes to mind is one with quadratic time complexity, i.e., for each node in the first linked list, a linear scan must be done in the second linked list. If any node from the first linked list is found in the second linked list (comparing addresses of nodes, not their data), that is the intersection point. However, if none of the nodes from the first list is found in the second list, that means there is no intersection point. Although this works, it is not efficient. A more efficient solution would be to store the nodes of the first linked list in a HashSet and then go through the second linked list nodes to check whether any of the nodes exist in the HashSet. This approach has a linear runtime complexity and linear space complexity. We can use a much better, i.e., O(m + n), linear time complexity algorithm that doesn’t require extra memory. To simplify our problem, let’s say both the linked lists are of the same size. In this case, you can start from the heads of both lists and compare their addresses. If these addresses match, it means it is an intersection point. If they don’t match, move both pointers forward one step and compare their addresses. Repeat this process until an intersection point is found, or both of the lists are exhausted. How do we solve this problem if the lists are not of the same length? We can extend the linear time solution with one extra scan on the linked lists to find their lengths. Below is the complete algorithm:

```
Find lengths of both linked lists: L1 and L2 Calculate the difference in length of both linked lists: d = |L1 - L2| Move head pointer of longer list 'd' steps forward Now traverse both lists, comparing nodes until we find a match or reach the end of lists
```

Code :tada:
```java

class Intersect{
  public static LinkedListNode intersect(LinkedListNode head1, LinkedListNode head2) {

    LinkedListNode list1node = null;
    int list1length = get_length(head1);
    LinkedListNode list2node = null;
    int list2length = get_length(head2);

    int length_difference = 0;
    if(list1length >= list2length) {
      length_difference = list1length - list2length;
      list1node = head1;
      list2node = head2;
    } else {
      length_difference = list2length - list1length;
      list1node = head2;
      list2node = head1;
    }

    while(length_difference > 0) {
      list1node = list1node.next;
      length_difference--;
    }

    while(list1node != null) {
      if(list1node == list2node) {
        return list1node;
      }

      list1node = list1node.next;
      list2node = list2node.next;
    }
    return null;
  }

  private static int get_length(
    LinkedListNode head) {      
    int list_length = 0;
    while(head != null) {
      head = head.next;
      list_length++;
    }
    return list_length;
  }
  public static void main(String[] args) {
    int [] a1 = {13,4};
    int [] a2 = {29, 23, 82, 11};
    LinkedListNode list_head_1 = LinkedList.createLinkedList(a1);
    LinkedListNode list_head_2 = LinkedList.createLinkedList(a2);
    LinkedListNode node1 = new LinkedListNode(12);
    LinkedListNode node2 = new LinkedListNode(27);

    LinkedList.insertAtTail(list_head_1, node1);
    LinkedList.insertAtTail(list_head_1, node2);
    
    LinkedList.insertAtTail(list_head_2, node1);
    
    System.out.print("List 1: ");
    LinkedList.display(list_head_1);
    System.out.print("List 2: ");
    LinkedList.display(list_head_2);

    LinkedListNode intersect_node = intersect(list_head_1, list_head_2);
    System.out.println(String.format("Intersect at %d", intersect_node.data));  
  }
}  
```

- Runtime complexity :

The runtime complexity of this solution is linear, O(m + n) Where m is the length of the first linked list and n is the length of the second linked list.

- Memory complexity :

The memory complexity of this solution is constant, O(1).

### Reverse Alternate K Nodes in a Singly Linked List
<hr>

Given a singly linked list and an integer 'k', reverse every 'k' element. If k <= 1, then the input list is unchanged. If k >= n (n is the length of linked list), then reverse the whole linked list.

- Description :

Given a singly linked list and an integer ‘k’, reverse every ‘k’ element. If `k <= 1`, then the input list is unchanged. If` k >= n` (n is the length of the linked list), then reverse the whole linked list.

- Hints :

Reverse the first k element, then move to the next k element.

**Solution**

Algorithmically, it is a simple problem, but writing code for this is a bit trickier as it involves keeping track of a few pointers. Logically, we break down the list to sub-lists each of size ‘k’. We’ll use the below pointers:

`reversed`: it points to the head of the output list.
`current_head`: head of the sub-list of size ‘k’ currently being worked upon.
`current_tail`: tail of the sub-list of size ‘k’ currently being worked upon.
`prev_tail`: tail of the already processed linked list (where sub-lists of size ‘k’ have been reversed).
We’ll work upon one sub-list of size ‘k’ at a time. Once that sub-list is reversed, we have its head and tail in `current_head` and `current_tail` respectively. If it was the first sub-list of size ‘k’, its head (i.e., `current_head`) is the head (i.e., `reversed`) of the output linked list. We’ll point `reversed` to `current_head` of the first sub-list. If it is the 2nd or higher sub-list, we’ll connect the tail of the previous sub-list to head of the current sub-list, i.e., update `next` pointer of the tail of the previous sub-list with the head pointer of current sub-list to join the two sub-lists.

- Code :tada:
```java

class ReverseK{
  static LinkedListNode reverseKNodes(LinkedListNode head, int k) {

    // if k is 0 or 1, then list is not changed
    if (k <= 1 || head == null) {
      return head;
    }

    LinkedListNode reversed = null;
    LinkedListNode prevTail = null;

    while (head != null && k > 0) {
      LinkedListNode currentHead = null;
      LinkedListNode currentTail = head;

      int n = k;
      while (head != null && n > 0) {
        LinkedListNode temp = head.next;
        head.next = currentHead;
        currentHead = head;

        head = temp;
        n--;
      }

      if (reversed == null) {
        reversed = currentHead;
      }

      if (prevTail != null) {
        prevTail.next = currentHead;
      }
      prevTail = currentTail;
    }

    return reversed;
  }

  public static void main(String[] args) {
    int[] v1 = new int[]{1, 2, 3, 4, 5, 6, 7};
    LinkedListNode listHead = LinkedList.createLinkedList(v1);
    System.out.print("Original list: ");
    LinkedList.display(listHead);

    listHead = reverseKNodes(listHead, 4);
    System.out.print("List reversed by 4: ");
    LinkedList.display(listHead);
  }
}  
```

- Runtime complexity :

The runtime complexity of this solution is linear, O(n).

- Memory complexity :

The memory complexity of this solution is constant, O(1).

### Merge K Sorted Lists
<hr>

- Problem Statement :

Given an array of ‘K’ sorted LinkedLists, merge them into one sorted list.

- Example 1 :
```
Input: L1=[2, 6, 8], L2=[3, 6, 7], L3=[1, 3, 4] Output: [1, 2, 3, 3, 4, 6, 6, 7, 8]
```
- Example 2 :
```
Input: L1=[5, 8, 9], L2=[1, 7] Output: [1, 5, 7, 8, 9]
```
- Solution : 

A brute force solution could be to add all elements of the given ‘K’ lists to one list and sort it. If there are a total of ‘N’ elements in all the input lists, then the brute force solution will have a time complexity of O(NlogN)* as we will need to sort the merged list. Can we do better than this? How can we utilize the fact that the input lists are individually sorted? If we have to find the smallest element of all the input lists, we have to compare only the smallest (i.e. the first) element of all the lists. Once we have the smallest element, we can put it in the merged list. Following a similar pattern, we can then find the next smallest element of all the lists to add it to the merged list.

The best data structure that comes to mind to find the smallest number among a set of ‘K’ numbers is a Heap. Let’s see how can we use a `heap` to find a better algorithm.

We can insert the first element of each array in a Min Heap.
After this, we can take out the smallest (top) element from the heap and add it to the merged list.
After removing the smallest element from the heap, we can insert the next element of the same list into the heap.
We can repeat steps 2 and 3 to populate the merged list in sorted order.

- Code :tada:
```java
import java.util.*;

class ListNode {
  int value;
  ListNode next;

  ListNode(int value) {
    this.value = value;
  }
}

class MergeKSortedLists {

  public static ListNode merge(ListNode[] lists) {
    PriorityQueue<ListNode> minHeap = new PriorityQueue<ListNode>((n1, n2) -> n1.value - n2.value);

    // put the root of each list in the min heap
    for (ListNode root : lists)
      if (root != null)
        minHeap.add(root);

    // take the smallest (top) element form the min-heap and add it to the result; 
    // if the top element has a next element add it to the heap
    ListNode resultHead = null, resultTail = null;
    while (!minHeap.isEmpty()) {
      ListNode node = minHeap.poll();
      if (resultHead == null) {
        resultHead = resultTail = node;
      } else {
        resultTail.next = node;
        resultTail = resultTail.next;
      }
      if (node.next != null)
        minHeap.add(node.next);
    }

    return resultHead;
  }

  public static void main(String[] args) {
    ListNode l1 = new ListNode(2);
    l1.next = new ListNode(6);
    l1.next.next = new ListNode(8);

    ListNode l2 = new ListNode(3);
    l2.next = new ListNode(6);
    l2.next.next = new ListNode(7);

    ListNode l3 = new ListNode(1);
    l3.next = new ListNode(3);
    l3.next.next = new ListNode(4);

    ListNode result = MergeKSortedLists.merge(new ListNode[] { l1, l2, l3 });
    System.out.print("Here are the elements form the merged list: ");
    while (result != null) {
      System.out.print(result.value + " ");
      result = result.next;
    }
  }
}
```

- Time complexity :

Since we’ll be going through all the elements of all arrays and will be removing/adding one element to the heap in each step, the time complexity of the above algorithm will be O(N*logK), where ‘N’ is the total number of elements in all the ‘K’ input arrays.

- Space complexity :

The space complexity will be `O(K)` because, at any time, our min-heap will be storing one number from all the ‘K’ input arrays


... (rest of your README)
