This solution works as follows:
We first handle some edge cases:
Negative numbers are not palindromes.
Single-digit numbers are always palindromes.
Numbers ending with 0 are palindromes only if they are 0.
We then reverse the number, but only up to its halfway point. This is done to avoid integer overflow and also to optimize the solution.
Finally, we compare the reversed number with the original number (or the original number divided by 10 for odd-length numbers).
This approach solves the problem without converting the integer to a string, satisfying the follow-up question. It has a time complexity of O(log x) because we process each digit of the number, and the number of digits is logarithmic to the value of x. The space complexity is O(1) as we only use a constant amount of extra space.