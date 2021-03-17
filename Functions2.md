# Exercise Functions 2

## Exercise 1
Write a function to find the Max of three numbers
## c
```c
#include  <stdio.h>

int MaxOfTwo (int x, int y){
if(x > y){
return x;
}
return y;
}
  
int MaxOfThree (int x, int y, int z){
int w = MaxOfTwo(z,MaxOfTwo(x,y));
return w;
}

int main(void) {
printf("%d",MaxOfThree(9,4,5));
return  0;
}
```
## python
```py
def max_of_two(x,y):
	if x > y:
		return x
	return y

  
def max_of_three(x,y,z):
	return max_of_two(x,max_of_two(y,z))
  
print("Max of three: " ,max_of_three(4,3,2))
```

## Exercise 2
Write a function to sum all the numbers in a list
## c
```c
#include  <stdio.h>

int sum_list (int num[], int size){

int total = 0;

for(int i = 0; i < size; i++){
total = total + num[i];
}

return total;
}

int list[ ] = {1,2,6,8,5,7,-6,-3};

int main(void) {
printf("%d",sum_list(list, sizeof(list)));  

return  0;

}
```
## python
```py
nums = [1,2,6,8,5,7,-6,-3]

def sum_list(nums):
	suma = 0
	for i in nums:
		suma = suma + i
	return suma
  

print("Sum of a list: " , sum_list(nums))
```
## Exercise 3
Write a function to multiply all the numbers in a list
## c
```c
#include  <stdio.h>

int mult_list (int num[ ], int x){

int total = 1;

for(int i = 0; i < x ; i++){
total = (total)*(num[i]);
}
  
return total;
}

int list[ ] = {1,2,6,8,5,7}; 

int main(void) {

int size = sizeof(list) / sizeof(list[0]);
printf("%d\n",mult_list(list,size));

return  0;
}
```
## python
```py
nums = [1,2,6,8,5,7,-6,-3]

def product_list(nums):
	total = 1
	for i in nums:
		total = total * i
	return total
  
print("product of a list: " , product_list(nums))
```
## Exercise 4
Write a  program to reverse a string
## c
```c
#include  <stdio.h>
#include  <string.h>
  
int InvertedString (char string[30]){
int x;
for(int i = 0;i<strlen(string); i++){
x =(strlen(string)-1) - i;
printf("%c",string[x]);
}

return  0;
}

char line[30];

int main(void){
  
printf("Enter a string\n");
fgets(line, sizeof(line), stdin);

InvertedString(line);
  
return  0;
}
```
## python
```py
def inverted_string (string1):

	string2 = ' '
	x = 0

	for i in range(0,len(string1)):
		x = (len(string1)-1) - i;
		string2 = string2 + string1[x]
	return string2
  
print("Reversed string ", inverted_string('This is a string'))
```
## Exercise 5
Write a function to calculate the factorial of a number (a non-negative integer). 
## c
```c
#include  <stdio.h>

int factorial (int num){

int c,f = 1;
for (c = 1; c <= num; c++){
f = f * c;
}
printf("Factorial of %d = %d\n", num, f);

return  0;
}

int n;

int main(void) {
printf("Enter a number to calculate its factorial\n");
scanf("%d", &n);
factorial(n);  

return  0;
}
```
## python
```py
def factorial(n):

	if n == 0:
		return 1
	else:
		return n * factorial(n-1)

print("Factorial of 6: ",factorial(6))
```
## Exercise 6
Write a function to check whether a number is in a given range
## c
```c
#include  <stdio.h>

int NumberInRange (int x, int y, int num){
if(num > x && num < y){
printf("%d is in the range", num);
} else{
printf("%d is not in the range", num);
}

return  0;
}
  
int n, x, y;
int main(void) {
printf("Enter a number\n");
scanf("%d", &n);
  
printf("Enter the first parameter of the range\n");
scanf("%d", &x);
  
printf("Enter the second parameter of the range\n");
scanf("%d", &y);

NumberInRange(x,y,n);
  
return  0;
}
```
## python
```py
def NumberInRange(num):

	if num in range(10):
		print( " %s is in the range" %str(num))
	else :
		print(" %s is not in the range." %str(num))
  
NumberInRange(5)
NumberInRange(15)
```
## Exercise 7
Write a function that accepts a string and calculate the number of upper case letters and lower case letters.
## c
```c
#include  <stdio.h>
#include  <string.h>

int UpperAndLowerLetters(char line[30]){
	int Upper = 0;
	int Lower = 0;

	for(int i = 0;i<strlen(line); i++){
		if(line[i] >= 'A' && line[i] <= 'Z'){
			Upper++;
		}
		else  if(line[i] >= 'a' && line[i] <= 'z'){
			Lower++;
		}
	}

printf("The number of upper letters is: %d\n",Upper);
printf("The number of lower letters is: %d\n",Lower);

return  0;
}

char line[30];

int main(void) {

	printf("Enter a string\n");
	fgets(line, sizeof(line), stdin);
 
	UpperAndLowerLetters(line);
	return  0;

}
```
## python
```py
def UpperAndLowerLetters(string):

	Upper = 0
	Lower = 0

	for i in string:
		if i.isupper():
			Upper = Upper + 1
		elif i.islower():
			Lower = Lower + 1

	print("The number of upper letters is:" ,Upper)
	print("The number of lower letters is:" ,Lower)


UpperAndLowerLetters('This is a String')
```
## Exercise 8
Write a function that takes a list and returns a new list with unique elements of the first list.
## c
```c
#include  <stdio.h>
#include  <string.h>

int list[ ] = {6,3,2,2,2,8,6};

int UniqueElements (int num[], int size){

int contador;
  
	for(int i=0; i<size; i++){
		contador=0;
		for(int j=0; j<(size+1); j++){
			if (i!=j){
				if(num[i]==num[j]){
					contador++;
				}
			}
		}	
		if(contador==0){
			printf("%d ",num[i]);
		}
	}

return  0;
}

int main(void) {

	int size = sizeof(list) / sizeof(list[0]);
	UniqueElements(list,size);

return  0;
}
```
## python
```py
def UniqueElements(nums):
	x = []
	for i in nums:
		if i not in x:
			x.append(i)
	return x

print(UniqueElements(nums))
```
## Exercise 9
Write a function that takes a number as a parameter and check the number is prime or not.
## c
```c
#include  <stdio.h>

int prime_number(int n){

	int x;  
	
	if(n == 1){
		x = 1;
	}
	if (n == 2){
		x = 0;
	} 
	else {
		for(int i=2; i<n;i++){
			if(n%i == 0){
				x = 1;
			break;
			} 
			else {
				x = 0;
			}
		}
	}
  
	if (x==1){
		printf("Is not a prime");
	}
	else {
		printf("Is a prime");
	} 

return  0;

}

int n, x, y;

int main(void) {
printf("Enter a number\n");
scanf("%d", &n);

prime_number(n);

return  0;

}
```
## python
```py
def prime_number(n):

	if (n==1):
		return False
	elif (n==2):
		return True;
	else:
		for x in range(2,n):
			if(n % x==0):
				return False
			return True

print("Number 13 is prime? ",prime_number(13))
print("Number 20 is prime? ",prime_number(20))
```
## Exercise 10
Write a program to print the even numbers from a given list.
## c
```c
#include  <stdio.h>

int list[ ] = {1,2,6,8,5,7};


int EvenNumbers(int num[], int size){
int x[30];
int j=0;
int i=0;

while (i<size){
	if(num[i]%2 == 0){
		x[j] += num[i];
		printf("%d ",x[j]);
		j++;
		i++;
}else{
	i++;	
}
} 

return  0;
}

int main(void) {

int size = sizeof(list) / sizeof(list[0]);
EvenNumbers(list,size);

return  0;
}
```
## python
```py
def Even_numbers(nums):

	x = []
	
	for i in nums:
		if (i%2) == 0:
			x.append(i)

	return x

print("The even numbers are: ", Even_numbers(nums))
```
## Exercise 11
Write a function to check whether a number is perfect or not.
## c
```c
#include  <stdio.h>
#include  <string.h>

int PerfectNumber (int num){

	int suma = 0;

	for(int i = 1; i<num; i++){
		if(num%i == 0){
			suma = suma + i;
		}
	}
	  
	if(suma == num){
		printf("%d is a perfect number\n",num);
	}
	else{
		printf("%d is not a perfect number\n",num);
	}
	
return  0;
}

int main(void) {

	PerfectNumber(6);
	PerfectNumber(20);

return  0;
}
```
## python
```py
def PerfectNumber(num):
	suma = 0

	for i in range(1, num):
		if num % i == 0:
			suma =suma + i

	if suma == num:
		print(num," is a perfect number")
	else:
		print(num," is not a perfect number")

PerfectNumber(6)
PerfectNumber(20)
```
## Exercise 12
Write a function that checks whether a passed string is palindrome or not.
## c
```c
#include  <stdio.h>
#include  <string.h>

int palindrome (char string[30]) {

int i = 0;
int j = strlen(string) - 1;

while (j > i){

if (string[i++] != string[j--]){
return  0;
}
}

return  1;

}

int main() {  

printf("%d\n",palindrome("ala"));
printf("%d\n",palindrome("hello"));

return  0;

}
```
## python
```py
def isPalindrome(string):
	str1 = 0
	str2 = len(string) - 1

	while str2 >= str1:
		if not string[str1] == string[str2]:
			return False
		str1 += 1
		str2 -= 1
	return True

print(isPalindrome('ala'))
print(isPalindrome('hello'))
```
