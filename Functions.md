Lets look back at our code:
```c
int main() {
	int a = 0;
	float b = 0.54f;
	return 0;
}
```

We will now look at the `int main()` bit.

This is the declaration of the `main` function, when you run your compiled program, it will start executing the `main` function.

We specify here that the `main` function has the _return type_ `int`. This means that it returns an integer to wherever it was called from. Inside the brackets we may place any parameters required by the function, allowing us to pass data in, although the process for this is slightly different with the `main` function in particular, so lets look at a different example:

```c
int sum(int a, int b) {
	return a + b;
}

int main() {
	printf("The sum of 4 and 5 is %d", sum(4, 5));

	return 0;
}
```

Here we declare another function `sum`, which takes two parameters, an `int` called `a`, and an `int` called `b`, and it returns another `int`. The line `return a + b;` means that the function will return the sum of `a` and `b`.

If we were to run this program, we would get:
```
The sum of 4 and 5 is 9
```

In `printf`, we call `sum`, and specify the values to pass into it's parameters inside the brackets as `4` and `5`, the sum of `4` and `5` is `9` so the function will return `9`.

If we had `int a = sum(3, 8);`, then the value of `a` would be `11`.

If we had `int a = sum(2, 7) + 3;`, the value of `a` would be `12`, which we would also get from doing `sum(sum(2, 7), 3)`. Do you see?

It might also interest you to know that `printf` and `scanf` are both functions, they both take a string as their first parameter, then `printf` will take the values to substitute into the string as the rest of its parameters, and `scanf` will take the address of the variable the input is to be stored into as its second parameter.

For example, the following can be done with `printf`:
```c
printf("Hello %d, I am %d", 2, sum(1, 4));
// Output: Hello 2, I am 5
```

And for `scanf`:
```c
int a;
scanf("%d", &a);
```

## Void return type
If you don't want a function to return anything, then specify its' return type as `void`, like:
```c
void do_something() {...}

int main() {
	do_something();  // Doesn't return anything
	return 0;
}
```


Next, on to pointers.
