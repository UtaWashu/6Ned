**Задача:**
**344.Write a function that reverses a string. The input string is given as an array of characters s.***
**Решение:**
```cpp
class Solution {
public:
    void reverseString(vector<char>& s) {
       int left = 0;
        int right = s.size() - 1;
        while (left < right) {
            swap(s[left], s[right]);
            left++;
            right--;
        } 
    }
};
```
**Задача:**
**412.Given an integer n, return a string array answer (1-indexed) where:**
**Решение:**
```cpp
class Solution {
public:
    vector<string> fizzBuzz(int n) {
       vector<string> answer;
        for (int i = 1; i <= n; i++) {
            if (i % 3 == 0 && i % 5 == 0) {
                answer.push_back("FizzBuzz");
            } else if (i % 3 == 0) {
                answer.push_back("Fizz");
            } else if (i % 5 == 0) {
                answer.push_back("Buzz");
            } else {
                answer.push_back(to_string(i));
            }
        }
        return answer; 
    }
};
```
**Задача:**
**1952.Given an integer n, return true if n has exactly three positive divisors. Otherwise, return false.**
**Решение:**
```cpp
class Solution {
public:
    bool isThree(int n) {
        int count = 0;
        for(int i = 1; i <= n; i++) {
            if(n % i == 0) {
                count++;
            }
            if(count > 3) {
                return false;
            }
        }
        return count == 3;
    }
};
```