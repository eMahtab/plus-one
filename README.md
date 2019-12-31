# Plus One

### Implementation

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
