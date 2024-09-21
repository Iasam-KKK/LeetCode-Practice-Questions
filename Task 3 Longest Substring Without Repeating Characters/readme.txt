1. We initialize an empty set char_set to store unique characters, max_length to keep track of the longest substring length, and left pointer for the start of our sliding window.
2. We iterate through the string using right pointer:
If the current character is already in the set, we remove characters from the left side of the window until we remove the duplicate.
We add the current character to the set.
We update max_length if the current window size is larger.
Finally, we return max_length.
This solution has a time complexity of O(n) where n is the length of the string, as we iterate through the string once. The space complexity is O(min(m, n)), where m is the size of the character set (at most 256 for ASCII), and n is the length of the string.