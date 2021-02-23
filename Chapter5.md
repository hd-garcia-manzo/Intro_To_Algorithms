# Exercise Chapter 5

## Exercise 5-1
Write a program that converts Centigrade to Fahrenheit.
 ```c
#include  <stdio.h>
//A program that converts Centigrade to Fahrenheit. 

char line[100];
float F; // Fahrenheit degrees
float C; // Centigrade degrees

int main(){
printf("Enter the temperature in Centigrade degrees\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%f", &C);

F = (C*9/5) + 32;

printf("temperature in Fahrenheit degrees: %f\n", F);

return (0);

}
```
## Exercise 5-2
Write a program to calculate the volume of a sphere.
 ```c
#include  <stdio.h>
//A program to calculate the volume of a sphere.

char line[100];
float R; // Sphere Radius
float vol; // Sphere volume
const  float pi = (3.1416); // Pi

int main(){
printf("Enter the radius of a sphere\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%f", &R);

vol = (1.33334)*(pi)*(R*R*R);
printf("The volume is: %f\n", vol);

return (0);
}
```
## Exercise 5-3
Write a program that prints the perimeter of a rectangle given its height and width.
 ```c
#include  <stdio.h>
//A program that prints the perimeter of a rectangle

char line[100];
float height; //the height of the rectangle
float width; //the width of the rectangle
float perimeter; // perimeter of the rectable

int main(){
printf("Enter the height\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%f", &height);

printf("Enter the width\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%f", &width);

perimeter = (width + height) * 2;
printf("The perimeter is %f\n", perimeter);

return (0);
}
```

## Exercise 5-4
Write a program that converts kilometers per hour to miles per h our
 ```c
#include  <stdio.h>
/* A program that converts kilometers per hour to miles per hour*/

char mychar[100];
float km; // kilometers
float miles; // miles

int main(){
printf("Enter the velocity in Km per hour\n");
fgets(mychar, sizeof(mychar), stdin);
sscanf(mychar, "%f", &km);

miles = km / 1.609;
printf("The velocity in miles per hour is: %f\n", miles);
return (0);

}
```
## Exercise 5-5

Write a program that takes hours and minutes as input, and then outputs the total number of minutes.
 ```c
#include  <stdio.h>
/* Program that takes hours and minutes as input, and then outputs the total number of minutes */
  
char line[100];
int hours; // Number of hours
int min; // Number of minutes
  
int main(){
printf("Enter the hours\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%d", &hours);

printf("Enter the minutes \n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%d", &min);

min = min + (hours*60);
printf("The total number of minutes: %d\n", min);

return (0);
}
```
## Exercise 5-6
Write a program that takes an integer as the number of minutes, and outputs the total hours and minutes
 ```c
#include  <stdio.h>
/* Program that takes an integer as the number of minutes, and outputs the total hours and minutes*/

char line[100];
int hours; // Number of hours
int min; // Number of minutes

int main(){
printf("Enter The total number of minutes\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%d", &min);

hours = min/60;
min = min - (hours*60);
printf("The total of hours: %d and minutes %d\n",hours, min);

return (0);
}
```
## Exercise 5-7
Free program
``` c
#include  <stdio.h>
// Program that converts pesos to dollars

float Pesos, dollar;
const  float Conver = 0.0481; //Conversion factor

int main() {
printf("Enter the amount in pesos\n");
printf("$");
scanf("%f", &Pesos);

dollar = Pesos * Conver;
printf("The amount in dollars is: %f\n",dollar);

return  0;
}
```
