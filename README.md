//Maximum sum of i*arr[i] among all rotations of a given array
package com.tata.shree;

class GFG {
	static int maxSum(int arr[], int n) {
		int res = Integer.MIN_VALUE;
		for (int i = 0; i < n; i++) {
			int curr_Sum = 0;
			for (int j = 0; j < n; j++) {

				int index = (i + j) % n;

				curr_Sum += j * arr[index];
			}
			res = Math.max(res, curr_Sum);
		}
		return res;

	}

	public static void main(String args[]) {
		int arr[] = { 4, 3, 8, 6 };
		int n = arr.length;
		System.out.println(maxSum(arr, n));
	}

}
