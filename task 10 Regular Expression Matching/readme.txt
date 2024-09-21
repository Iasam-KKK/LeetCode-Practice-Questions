This solution uses a 2D DP table where dp[i][j] represents whether the first i characters of s match the first j characters of p. Here's how it works:
We initialize the DP table with false values.
We set dp[0][0] = true because an empty pattern matches an empty string.
We handle patterns that start with * in the first row of the DP table.
We then fill the DP table:
If the current characters match or the pattern character is '.', we take the value from the diagonal left (i.e., dp[i-1][j-1]).
If the pattern character is '', we have two cases:
We can ignore the '' and the character before it (i.e., dp[i][j-2]).
Or, if the character before '' matches the current character in s, we can use the '' to match one or more characters (i.e., dp[i-1][j]).
The final answer is in dp[m][n], where m and n are the lengths of s and p respectively.
This solution has a time complexity of O(mn) and a space complexity of O(mn), where m and n are the lengths of s and p respectively.