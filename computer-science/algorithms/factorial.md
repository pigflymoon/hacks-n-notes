# Factorial

A *factorial* is the product of the integers 1 through $$n$$.

For example: $$5! = 1 * 2 * 3 * 4 * 5 = 120$$

It is useful to calculate the amount of different combinations of a set. Specially useful when doing *permutations and combinations*.

## Iterative factorial

```javascript
var factorial = function(n) {
    var result = 1;
    
    for(var i = 1; i <= n; i++) {
        result *= i;
    }

    return result;
};
```

## Recursive factorial

We don't need to run a loop.

```javascript
var factorial = function(n) {
	// base case: 
	if (n === 0) {
	    return 1;
	}
	
	// recursive case:
	if (n > 1) {
	    return n * factorial(n - 1);    
	}
	
	return 1;
};
```
