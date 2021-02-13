# Exercise Chapter 4

## Exercise 4-1
Write a program to print your name, social security number, and date of birth.
 ```c
#include  <stdio.h>

int main(void) {

printf("Name: Hugo Daniel Garcia Manzo\n");
printf("ID: 2009059\n");
printf("Birth: 21/07/98\n");

return  0;
}
```
## Exercise 4-2
Write a program to print a block E using asterisks (*), where the E has a height of seven characters and a width of five characters.
 ```c
#include  <stdio.h>

int main(void) {

printf("*****\n");
printf("*\n");
printf("*\n");
printf("*****\n");
printf("*\n");
printf("*\n");
printf("*****\n");

return  0;
}
```
## Exercise 4-3
Write a program to compute the area and perimeter of a rectangle with a width of three inches and a height of five inches. What changes must be made to the program so that it works for a rectangle with a width of 6.8 inches and a length of 2.3 inches?
 ```c
#include  <stdio.h>

float height;
float width;
float area;
float perimeter;

int main(void) {
	height = 6.8;
	width = 2.3;
	area = (height*width);
	perimeter = (height*2)+(width*2);

printf("Area: %f\n",area);
printf("Perimeter: %f\n",perimeter);

return  0;
}
```
## Exercise 4-4
Write a program to print "HELLO" in big block letters; each letter should have a height of seven characters and width of five characters.
 ```c
#include  <stdio.h>

int main(void) {
printf("*   * ***** *     *     *****\n");
printf("*   * *     *     *     *   *\n");
printf("*   * *     *     *     *   *\n");
printf("***** ***** *     *     *   *\n");
printf("*   * *     *     *     *   *\n");
printf("*   * *     *     *     *   *\n");
printf("*   * ***** ***** ***** *****\n");
return  0;

}
```
## Exercise 4-5
Write a program that deliberately makes the following mistakes: 
- Prints a floating-point number using the %d conversion. 
- Prints an integer using the %f conversion. 
- Prints a character using the %d conversion
 ```c
#include  <stdio.h>

float fnumber;
int inumber;
char charletter;

int main(void) {
	fnumber = 45.20;
	inumber = 36;
	charletter = 'Z';

printf("This is the wrong form to print a float number: %d\n", fnumber);

printf("This is the wrong form to print an int number: %f\n", inumber);

printf("This is the wrong form to print a char: %d\n", charletter);

  

printf("This is the correct form to print a float number: %f\n", fnumber);

printf("This is the correct form to print an int number: %d\n", inumber);

printf("This is the correct form to print a char: %c\n", charletter);

return  0;

}
```
## Exercise 4-6
Write a program to caculate the average of three scores.
 ```c
#include  <stdio.h>

float score1, score2, score3;

int main(void) {
	score1 = 9.3;
	score2 = 7.5;
	score3 = 8.0;

printf("Your scores are: %f, %f and %f\n", score1, score2,score3);

printf("The average is: %f\n", ((score1+score2+score3)/3));

return  0;

}
```
