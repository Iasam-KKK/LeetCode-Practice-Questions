This solution works as follows:
We initialize a result variable to store the reversed number.
We use a while loop to process each digit of the input number x.
In each iteration:
We extract the last digit using x % 10.
We check for potential overflow before adding the new digit to the result.
If no overflow, we add the digit to the result and remove it from x.
We return the final reversed number.
The overflow check is crucial here. We check if adding the next digit would cause an overflow by comparing the current result with INT_MAX / 10 and INT_MIN / 10. If an overflow would occur, we return 0 as specified in the problem statement.
This solution handles all the requirements:
It works for both positive and negative numbers.
It returns 0 if the reversed number would overflow a 32-bit integer.
It doesn't use any 64-bit integers, adhering to the constraint mentioned in the problem.
The time complexity of this solution is O(log x), where x is the input integer, as we process each digit of the number. The space complexity is O(1) as we only use a constant amount of extra space.