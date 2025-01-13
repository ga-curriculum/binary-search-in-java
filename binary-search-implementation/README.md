<h1>
  <span class="headline">Binary Search in Java</span>
  <span class="subhead">Binary Search</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to implement binary search algorithm using Java code.
## Demo of binary search algorithm implementation
```java
public class BinarySearch {
    public static int binarySearch(int[] array, int target) {
        int low = 0;
        int high = array.length - 1;

        while (low <= high) {
            int mid = low + (high - low) / 2;

            if (array[mid] == target) {
                return mid; // Target found
            } else if (array[mid] < target) {
                low = mid + 1; // Ignore left half
            } else {
                high = mid - 1; // Ignore right half
            }
        }
        return -1; // Target not found
    }

    public static void main(String[] args) {
        int[] sortedArray = {2, 3, 5, 7, 11, 13, 17};
        int target = 7;

        int result = binarySearch(sortedArray, target);
        if (result != -1) {
            System.out.println("Element found at index: " + result);
        } else {
            System.out.println("Element not found in the array.");
        }
    }
}
```
