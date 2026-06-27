# Valid Palindrome

**LeetCode:** 125 - Valid Palindrome

---

## Problem Statement

Given a string `s`, return `True` if it is a palindrome; otherwise, return `False`.

A palindrome is a string that reads the same forwards and backwards.

### Examples

```text
Input:  "madam"
Output: True

Input:  "racecar"
Output: True

Input:  "hello"
Output: False
```

---

# Brute Force Approach

## Idea

1. Reverse the string.
2. Compare the reversed string with the original.
3. If both are equal, it is a palindrome.
4. Otherwise, it is not a palindrome.

---

## Using Python Built-in Slicing

```python
def is_palindrome(s):
    reversed_string = s[::-1]

    if s == reversed_string:
        return True
    else:
        return False


text = input("Enter a string: ")

if is_palindrome(text):
    print("Valid Palindrome")
else:
    print("Not a Valid Palindrome")
```

---

## Without Using Python Built-in Reverse

```python
def is_palindrome(s):
    reversed_str = ""

    for char in s:
        reversed_str = char + reversed_str

    if s == reversed_str:
        return True
    else:
        return False


text = input("Enter a string: ")

if is_palindrome(text):
    print("Valid Palindrome")
else:
    print("Not a Valid Palindrome")
```

The loop executes as follows:

Each new character is inserted at the **front** of the string:

```python
reversed_str = char + reversed_str
```



| Character | Previous `reversed_str` | New `reversed_str` |
| --------- | ----------------------- | ------------------ |
| H         | ""                      | H                  |
| E         | H                       | EH                 |
| L         | EH                      | LEH                |
| L         | LEH                     | LLEH               |
| O         | LLEH                    | OLLEH              |



### Time Complexity

`O(n)`

### Space Complexity

`O(n)`

---

# Optimized Approach (Two Pointers)

## Idea

Instead of creating another string, compare characters from both ends of the string.

* Place one pointer at the beginning.
* Place another pointer at the end.
* Compare both characters.
* If they are different, immediately return `False`.
* Otherwise, move both pointers toward the center.
* If all characters match, return `True`.

Since Python strings are immutable, we don't modify the string. We simply compare characters using their indices.

---

## Visualization

```text
M A D A M
↑       ↑
L       R

M == M ✓

  ↑   ↑
  A   A

A == A ✓

    ↑
    D

Pointers meet.

Palindrome ✓
```

---

## Algorithm

```text
left = 0
right = len(s) - 1

while left < right

    if s[left] != s[right]
        return False

    left += 1
    right -= 1

return True
```

---

## Python Code

```python
def is_palindrome(s):
    left = 0
    right = len(s) - 1

    while left < right:
        if s[left] != s[right]:
            return False

        left += 1
        right -= 1

    return True


text = input("Enter a string: ")

if is_palindrome(text):
    print("Valid Palindrome")
else:
    print("Not a Valid Palindrome")
```

---

## Time Complexity

`O(n)`

Each character is visited at most once.

---

## Space Complexity

`O(1)`


# Conclusion

### Brute Force

Create a reversed copy of the string and compare it with the original. This approach is simple to understand but requires additional memory.

### Optimized

Use the **Two Pointer Technique** to compare characters from both ends of the string without creating another string. This achieves **O(n)** time complexity with **O(1)** extra space, making it the preferred solution for coding interviews.
