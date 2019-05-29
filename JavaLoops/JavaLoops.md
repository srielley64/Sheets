# Java Loops
---
## While Loops
The easiest looping structure is `while()`.  It takes a conditional statement between the '(' and ')'.

```Java
while ( true ) {
  // do something
}
```
---

### While example
```Java
int i = 0;
int maxCount = 10;
int sum = 0;  
while ( i <= maxCount ) {
  sum += i;
  System.out.print(sum+" ");
}
```

```
0 1 3 6 10 15 21 28 36 45 55
```

This will keep looping until the conditional resolves to `false`.

---
## Do...While() Loops
As with `while()`, its conditional test has to be true to keep looping.  It is just like the `while()` loop but it allows for one run-through before the test.

```Java  
do {
  // do something
} while (true);
```
---
### Do...While() example

```Java
int i = 0;
int maxCount = 10;
int sum = 0;
do {
  sum+=i++
} while ( i < maxCount);
```

```
0 1 3 6 10 15 21 28 36 45 55
```
---
## When would you use While() and Do...While()?

Generally, it is up to your coding style. I normally use `do...while()` when I want to process something each time *before* the test is run.  Otherwise, I use `while()`.

---
## For Loops
For loops are the equivalence of a while loop but a tad more compressed.

```Java  
for (init; true; finish) {
  // do something
}
```
- `init` is done before the loop
- `true` is loop conditional
- `finish` is what is done before the end of the loop
---
### For example
```Java  
int maxCount = 10;
int sum = 0;
for (int i = 0; i <= maxCount; i++) {
  sum += i;
  System.out.print(sum+" ");
}
```
```
0 1 3 6 10 15 21 28 36 45 55
```
---
## For Each
There is a special case for the `For Each` loop.  It is great for dealing with items that have `iterators`.  

```Java
for (Class name : Collection) {
  // do something
}
```
- Class: Class name
- name: variable name
- Collection: something that has an `Iterator`

It can be used on primitive arrays and any object that creates an `Interator` object.  We will cover this in more detail later.

---
### For Each example
```Java  
int[] arrayInt = {0,1,2,3,4,5,6,7,8,9,10};
int sum = 0;
for (int aInt : arrayInt) {
  sum += aInt;
  System.out.println(sum);
}
```
```
0 1 3 6 10 15 21 28 36 45 55
```
