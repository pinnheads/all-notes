> #algorithms #bigO #CS #data-structures 

Before learning about [[Algorithms]] we need to learn about a concept called Big O. This is how we measure or explain the time and performance of our algorithms.

## What is Big O?

- Big O is a **way to categorize your algorithms time** or memory requirements based on input.
- It is not meant to be an exact measurements, instead it is meant to generalize the growth of your algorithm.
- For example, when someone says O(N) (Oh of n) they mean your algorithm will grow linearly based on the input.
## Why do we use it?

1. To make good decisions on which data structures and algorithms to use.
2. Knowing how an algorithm will perform with different parameters helps us in creating the best possible program that runs fast and doesn't use too much memory.
### Example program

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; i++) {
		sum += n.charCodeAt(i);
	}
	return sum;
}
```
- The run time for the code snippet above is O(N). Here is the reasons why:
	- There is a single for loop that goes over the string 'n' and adds till the length of the string.
	- If the string is of length 5 the loop runs 5 times, if the length is 10 then the loop runs 10 times and so on.
	- This shows a linear growth in the time and space complexity and is donated by O(N)
	  
   ![[linear-growth-complexity.png]]

#### Some more examples

- O(N)
```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; i++) {
		sum += n.charCodeAt(i);
	}
	
	for (let i = 0; i < n.length; i++) {
		sum += n.charCodeAt(i);
	}
	return sum;
}
```

- O(N^2)

```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; i++) {
		for (let j = 0; j < n.length; j++) {
			sum += n.charCodeAt(i);
		}
	}
	return sum;
}
```

- O(N^3)
```typescript
function sum_char_codes(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; i++) {
		for (let j = 0; j < n.length; j++) {
			for (let k = 0; k < n.length; k++) {
				sum += n.charCodeAt(i);
			}
		}
	}
	return sum;
}
```
