# Curious

A collection of code implementations for things that interest me.

## Contents

## 1. Possible Triangles

How many different triangles can exist if we only consider integer angles (in degrees)?

### The Solution
```python
triangles = set()

for first in range(1,178):
    for second in range(1,180-first):
        third = 180- (first + second)
        tri = tuple(sorted((first, second , third)))
        triangles.add(tri)

print(len(triangles))
  # Output: 2700
```

### How It Works

1. **Basic Triangle Properties**
   - Sum of angles must be exactly 180°
   - Each angle must be a positive integer
   - Angles like (30°, 60°, 90°) and (90°, 60°, 30°) are considered the same triangle

2. **Code Breakdown**
   - First loop: Tries angles from 1° to 178°
   - Second loop: Only checks up to what's possible given first angle
   - Third angle: Calculated directly as 180° - (first + second)
   - `sorted()` handles rotations of the same triangle
   - `set` ensures each unique triangle is counted only once

3. **Optimizations**
   - Avoids unnecessary iterations by calculating third angle
   - Range limits prevent impossible combinations
   - `sorted` tuple in set eliminates rotational duplicates

### Result
There are exactly 2700 different possible triangles with integer angles!


## 2. Monkey Type

This code simulates a classic thought experiment: how long would it take a monkey randomly typing on a keyboard to write a specific word?

### Functionality

This program lets you define a target word and then simulates a monkey randomly hitting keys until it types the word correctly.

**Example:**

```
your word?: hello
serpenp
udkknu
yhgjlo
hello
Used 4 tries
```

This example shows that it took the program (monkey) 4 attempts to generate the word "hello".

### Note

This program is a simplified simulation. It doesn't account for factors like real-world keyboards or the monkey's typing speed. It serves as a fun demonstration of random chance and the vast number of attempts it could take to achieve a specific outcome.

## 3. Get domain
This code grabs domain from urls using regular expression. Nothing to add much.

## Usage

Each file is self-contained and can be run independently using Python 3.x.

## Future Additions

The repository will be updated with new implementations as more interesting problems are explored and solved.

