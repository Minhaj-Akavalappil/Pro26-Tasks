Intuition
We want to find two numbers that add up to a given target.
As we look at each number, if we already know a number we've seen before that would add up to the target with the current number, we can immediately return the indices.

Approach
Use a hash map (dictionary) to store each number and its index as we iterate through the array.
For each number, calculate its complement (target - num).

If the complement already exists in the dictionary, return the current index and the stored index of the complement.

Otherwise, store the current number with its index in the dictionary and continue.

This way, we only loop through the list once.

Complexity
Time complexity:𝑂(𝑛)
We traverse the list only once, and dictionary lookups take constant time 𝑂(1) on average.

Space complexity:𝑂(𝑛)
In the worst case, we store all n numbers in the dictionary.
