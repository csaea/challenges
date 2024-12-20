# Binary and Hexadecimal Challenges and Explanations: 

## Challenge 1.1: Binary Translation

1. Think of a 7-10 letter word and encode it in binary. You may only use an ASCII table. 

2. Give it to a partner and have them decode it into plaintext. 

## Challenge 1.2: Decimal to Binary Algorithm 

Write a Python algorithm that converts a decimal number its binary representation.

## Three possible solutions to the Binary Algorithm 

### Pseudocode:

1. **Initialize binary string**: Start with an empty variable string called 'binary' for accumulating the 0s and 1s.
2. **While loop**: Repeatedly divide the number by 2 and prepend the remainder (either 0 or 1) to 'binary' variable.
3. **Update the number**: Use integer division on the number, and and update it.
4. **Final output**: After the loop ends, print the final binary string.

### Example of Execution:
For `num = 13`:
- 13 ÷ 2 → 6, remainder 1 (binary = '1')
- 6 ÷ 2 → 3, remainder 0, (binary = '01')
- 3 ÷ 2 → 1, remainder 1, (binary = '101')
- 1 ÷ 2 → 0, remainder 1, (binary = '1101')

Final output: `'1101'`.

### Python code 

```python
#Python's Built-In bin() function 
print("\nBuilt In Solution:")

def Built_in_solution(num):
    binary_conversion = bin(num)[2:]
    print(binary_conversion)

Built_in_solution(13)

# Custom iteration and Accumulation
print("\nIterative Solution") 
def Iterative_solution(num):
    binary = ''
    while num > 0:
        binary = str(num % 2) + binary 
        print(binary)
        num = num // 2
    print(binary) 

Iterative_solution(13)

# Recursive Solution
print("\nRecursive solution:")
def Recursive_solution(num):

    if num >= 1: 
        Recursive_solution(num // 2)
        
        print (num % 2)

Recursive_solution(13)
```
