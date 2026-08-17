# Today, I understand why the bugs happened in 2 previous programs.

## 1. What happens if we assign an element at index exceeding the length in c?
- Actually, C language doesn't check the array bounds checking and also it won't increase the size of the array.
- The behaviour of the program can be undefined.
- We cannot predict exactly what happens; therefore, the output we expect may not happen.

## 2. How does a 2 digit integer is stored as char in C?
- When a two digit number is converted into char by adding '0' character to it. It gets converted into char of a specific ASCII value.
```C
int num = 20;
char ch = num + '0'; // 20 + 48 = 68 (D)
printf("%d, %c", num, ch); // 20, D
```
- When we again convert into integer by subtracting with '0', we will get the difference as the integer initially we had.
```C
int transformNum = ch - '0'; // 68 - 48
printf("%d", transformNum); // 20
```
- But this method only works for the integers when converted into char which doesn't exceed the last ASCII value 127.
```C
int num = 80;
char ch = num + '0'; // 80 + 48 = 128
int transformNum = ch - '0'; // Unexpected value
printf("%d, %c, %d", num, ch, transformNum); // 80, , ,
```