# 🔹 Problem: Reverse String

**Link to problem:** [LeetCode - Reverse integer](https://leetcode.com/problems/reverse-integer/)

## 💡 Description:
Write a function that reverses a integer. 
## 🧠 Solution (Java):
```java
class Solution {
    public int reverse(int x) {
        int res=0;
        while(x!=0){
           int rem=x%10;
           if (res > Integer.MAX_VALUE / 10 || res < Integer.MIN_VALUE / 10) {
                return 0;
            }

            res=res*10+rem;
            x/=10;
        }
        return res;
    }
}
