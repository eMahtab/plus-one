# Plus One
# https://leetcode.com/problems/plus-one

Given a non-empty array of digits representing a non-negative integer, plus one to the integer.

The digits are stored such that the most significant digit is at the head of the list, and each element in the array contain a single digit.

You may assume the integer does not contain any leading zero, except the number 0 itself.

```
Example 1:

Input: [1,2,3]
Output: [1,2,4]
Explanation: The array represents the integer 123.

Example 2:

Input: [4,3,2,1]
Output: [4,3,2,2]
Explanation: The array represents the integer 4321.
```
# Key Points :
Lets think about some of the inputs e.g. `[1] , [2], [8], [9], [1, 0], [1, 1], [1, 9], [1, 2, 9], [9, 2, 9], [9, 9, 9]`

# Implementation

```java
import java.util.Arrays;

public class App {

	public static void main(String[] args) {
		int[] nums1 = {1, 2, 3};
		int[] nums2 = {9};
		int[] nums3 = {9, 9};
		int[] nums4 = {1, 0, 0, 9};
		System.out.println(Arrays.toString(plusOne(nums1)));
		System.out.println(Arrays.toString(plusOne(nums2)));
		System.out.println(Arrays.toString(plusOne(nums3)));
		System.out.println(Arrays.toString(plusOne(nums4)));
	}
	
	public static int[] plusOne(int[] digits) {
                if(digits == null || digits.length == 0)
                    return digits;
            
		for(int i = digits.length - 1; i >= 0; i--) {
			if(digits[i] < 9) {
			     digits[i] += 1;
			     return digits;
			}
			digits[i] = 0;
		}
		int[] res = new int[digits.length + 1];
		res[0] = 1;
		return res;
	}
}
```
Above implementation have runtime complexity of O(n) and space complexity of O(1)
```
Runtime Complexity = O(n)
Space Complexity   = O(1)
```
