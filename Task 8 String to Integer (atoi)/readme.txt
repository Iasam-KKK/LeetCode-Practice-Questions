This implementation follows the algorithm described in the problem statement:
We start by skipping any leading whitespace characters.
We then check for a sign ('+' or '-') and set the sign variable accordingly.
We read in the digits, converting them to an integer value. We use a long long to temporarily store the result to handle potential overflow.
While reading digits, we continuously check for overflow conditions. If the result exceeds the 32-bit integer range, we return the appropriate boundary value (INT_MAX or INT_MIN).
Finally, we return the result as a 32-bit integer, applying the sign.
This implementation handles all the given examples and constraints:
It ignores leading whitespace.
It handles both positive and negative numbers.
It stops reading at the first non-digit character after the optional sign.
It handles overflow by clamping to INT_MAX or INT_MIN.
It returns 0 if no valid conversion could be performed.
The time complexity of this solution is O(n), where n is the length of the input string, as we potentially need to scan the entire string once. The space complexity is O(1) as we only use a constant amount of extra space.