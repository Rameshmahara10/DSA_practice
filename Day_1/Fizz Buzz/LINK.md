# 🔹 Problem: Fizz Buzz

**Link to problem:** [LeetCode - Fizz Buzz](https://leetcode.com/problems/fizz-buzz/)

## 💡 Description:
Given an integer n, return a string array answer (1-indexed) where:

answer[i] == "FizzBuzz" if i is divisible by 3 and 5.
answer[i] == "Fizz" if i is divisible by 3.
answer[i] == "Buzz" if i is divisible by 5.
answer[i] == i (as a string) if none of the above conditions are true.

## 🧠 Solution (Java):
```java
class Solution {
    public List<String> fizzBuzz(int n) {
        String[] answer=new String[n];
        for(int i=0;i<n;i++){
            if(((i+1)%3==0) &&((i+1)%5==0)){
                answer[i]="FizzBuzz";
            }
            else if((i+1)%3==0){
                answer[i]="Fizz";
            }
            else if((i+1)%5==0)
            {
                answer[i]="Buzz";
            }
            else{
                answer[i]=String.valueOf(i+1);
            }

        }
        return  Arrays.asList(answer);
    }
}
