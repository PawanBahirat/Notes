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

- **Solution**

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

- **Solution 2**
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
... (rest of your README)
