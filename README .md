# Subarray Sum Equals K

This repository contains a C++ solution to find the number of subarrays in a given array that sum up to a target value `k`. The solution uses an optimal approach with hashing to achieve efficient performance.

## Problem Description

Given an array of integers `nums` and an integer `k`, return the total number of continuous subarrays whose sum equals `k`.

### Example
```
Input: nums = [9,4,20,3,10,5], k = 33
Output: 2
Explanation: The subarrays with sum 33 are [9,4,20] and [20,3,10].
```

## Solution

The repository includes a C++ implementation in the file `hashing_subarray_sum_eqauls_K.cpp`. Two approaches are provided:

1. **Brute Force Approach** (Commented out)
   - Time Complexity: O(n²)
   - Space Complexity: O(1)
   - Iterates through all possible subarrays to check if their sum equals `k`.

2. **Optimal Approach** (Using Hashing)
   - Time Complexity: O(n)
   - Space Complexity: O(n)
   - Uses a prefix sum technique combined with an unordered map to store the frequency of prefix sums. This allows for efficient counting of subarrays with sum `k`.

### How the Optimal Solution Works
- Compute the prefix sum for each index in the array.
- Use an unordered map to store the frequency of prefix sums encountered.
- For each prefix sum, check if there exists a previous prefix sum such that `prefixSum[j] - k` exists in the map. If it does, add its frequency to the count.
- Update the map with the current prefix sum's frequency.

## Files
- `hashing_subarray_sum_eqauls_K.cpp`: Contains the C++ code with both brute force (commented) and optimal solutions.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Sanju-1114/subarray-sum-equals-k.git
   ```
2. Compile and run the C++ code:
   ```bash
   g++ hashing_subarray_sum_eqauls_K.cpp -o subarray_sum
   ./subarray_sum
   ```
3. The program will output the number of subarrays with sum equal to `k` for the example input.

## Example Input/Output
For the input:
```cpp
vector<int> vec = {9,4,20,3,10,5};
int k = 33;
```
Output:
```
2
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an issue for any improvements or bug fixes.

## License
This project is licensed under the MIT License.