# 🔹 Problem: Happy Number
**Link to problem:** [LeetCode - HAPPY NUMBER](https://leetcode.com/problems/happy-number/)
## 💡 Description:
Write an algorithm to determine if a number n is happy. Return true if n is a happy number, and false if not.



## 🧠 Solution (Java):
```java
class Solution {
    public int sq(int x) {
        int s = 0;
        while (x != 0) {
            int d = x % 10;
            s += d * d;
            x /= 10;
        }
        return s;
    }

    public boolean isHappy(int n) {
        int slow = n;
        int fast = sq(n);

        while (fast != 1 && slow != fast) {
            slow = sq(slow);         
            fast = sq(sq(fast));     
        }

        return fast == 1;
    }
}
