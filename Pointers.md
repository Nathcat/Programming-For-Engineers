Ah. The best part of C. The infamous _Pointer_.

Remember how a variable is stored at a location in memory? Well a pointer is another variable, which contains the _memory address_ of another bit of data, like a variable. We declare pointers like so:

```c
int a = 5;
int* pA = &a;
```

Here, `a` is a variable containing an `int`, and `pA` is a variable containing an `int*`, which is a pointer to an `int` type. We define `pA` to contain `&a`, the `&` operator returns the address of a variable, so `pA` contains the address of `a`.

Now, we can use pointers to get values, and pass references to the same value, for example:

```c
int b = *pA;  // b will equal the value AT THE MEMORY ADDRESS WHICH pA CONTAINS
```

```c
void foo(int* pA) {
	*pA = 5;  // Sets the value at the memory address which pA points to
}

int main() {
	int a = 10;
	foo(&a);
	// a is now 5
	return 0;
}
```

Placing the `*` before a pointer _de-references_ the pointer, and allows the use / manipulation of the value which the pointer "points" to.
