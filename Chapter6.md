# Exercise Chapter 6

## Exercise 6-1
Write a program to find the square of the distance between two points. (For a more advanced problem, find the actual distance. This problem involves u sing the standard function sqrt. Use your help system to find out more about how to use this function.)
```c
#include  <stdio.h>
#include  <math.h>

/*A program to find the square of the distance between two
points. (For a more advanced problem, find the actual distance.*/

char line[100];

//The coordinates
double X1, Y1;
double X2, Y2;

double Sqr1,Sqr2; //Auxiliars
double distance;

int main(void) {
	printf("Enter the first point separated with a space (X Y)\n");
	fgets(line, sizeof(line), stdin);
	sscanf(line,"%lf %lf", &X1, &Y1);
	
	printf("Enter the second point separated with a space (X Y)\n");
	fgets(line, sizeof(line), stdin);
	sscanf(line,"%lf %lf", &X2, &Y2);

	printf("The point 1 is: X=%lf , Y=%lf\n", X1, Y1);
	printf("The point 2 is: X=%lf , Y=%lf\n", X2, Y2);
	  
	//The squares of the sums
	Sqr1 = pow((X2-X1),2);
	Sqr2 = pow((Y2-Y1),2);
	  
	distance = (Sqr1+Sqr2);
	distance = sqrt(distance);

	printf("The distance is: %lf\n", distance);

	return  0;

}
```
## Exercise 6-2
A professor generates letter grades using.
### Grade Values 
| % Right | Grade |
| -- | --|
| 0-60| F |
|61-70 | D |
|71-80 |C |
|81-90 |B |
|91-100| A|

 Given a numeric grade, print the letter.
```c
#include  <stdio.h>

/* A program that given a numeric grade, print the letter.*/

char line[100];
int Ngrade; // numeric grade
char grade;
int error = 0;
  
int main(void) {
	printf("Enter the numeric grade\n");
	fgets(line, sizeof(line), stdin);
	sscanf(line, "%d", &Ngrade);
	  
	if(Ngrade<=60 && Ngrade>0){
	grade = 'F';
	}

	if(Ngrade>60 && Ngrade<=70){
	grade = 'D';
	}

	if(Ngrade>70 && Ngrade<=80){
	grade = 'C';
	}

	if(Ngrade>80 && Ngrade<=90){
	grade = 'B';
	}

	if(Ngrade>90 && Ngrade<=100){
	grade = 'A';
	}

	//if the numeric grade is less than 0 o greater than 100
	if(Ngrade<0 || Ngrade>100){
	printf("Error\n");
	error = 1;
	}

	if(error == 0){
	printf("The grade is: %c\n",grade);
	}
	  
	return  0;
}
```
## Exercise 6-3
Modify the pre vious program to print a + or - after the letter grade, based on the last digit of the score. The modifiers are listed in Table.
Grade Modification Values 
|Last digit| Modifier|
| -- | ---|
 |1-3| - |
 |4-7| nothing|
 | 8-0 |+|
 For example, 81=B-, 94=A, and 68=D+. Note: An F is only an F. There is no F+ or F-.
```c
#include  <stdio.h>
#include  <string.h>

int Ngrade; // numeric grade
char line[100];
char grade[50];
int error = 0;
int lastN; // last number

int main(void) {
	printf("Enter the numeric grade\n");
	fgets(line, sizeof(line), stdin);
	sscanf(line, "%d", &Ngrade)
	  
	if(Ngrade<=60 && Ngrade>0){
		strcpy(grade,"F");
	}

	if(Ngrade>60 && Ngrade<=70){
		strcpy(grade,"D");
	}
	
	if(Ngrade>70 && Ngrade<=80){
		strcpy(grade,"C");
	}
	
	if(Ngrade>80 && Ngrade<=90){
		strcpy(grade,"B");
	}
	
	if(Ngrade>90 && Ngrade<100){
		strcpy(grade,"A");
	}

	if(Ngrade==100){ //Especial case
		strcpy(grade,"A+");
	} 

	if(Ngrade<0 || Ngrade>100){
		printf("Error\n");
		error = 1;
	}
	  
	lastN = (line[1]-'0');

	//Depending on the rating range add - or +
	if(Ngrade>60){
		if(lastN>=1 && lastN<=3){
			strcat(grade,"-");
		}
		if(lastN>=8){
			strcat(grade,"+");
		}
	}

	if(error == 0){
		printf("The grade is: %s\n",grade);
	}

	return  0;
}
```

## Exercise 6-4
Given an amount of money (less than $1.00), compute the number of quarters, dimes, nickels, and pennies needed.
```c
#include  <stdio.h>

/*Given an amount of money (less than $1.00), compute the number
of quarters, dimes, nickels, and pennies needed.*/
  
char line[100];
float num;
int quarters = 0;
int dimes = 0;
int nickels = 0;
int pennies = 0;

int main(void) {
	printf("enter a number less than $1.00\n");
	printf("$");
	fgets(line, sizeof(line), stdin);
	sscanf(line,"%f",&num);

	//subtract the quarters and count how many times it is subtracted.
	while(num>=0.25){
		num = num - 0.25;
		quarters = quarters + 1;
	}

	//subtract the dimes and count how many times it is subtracted.
	while(num>=0.10 && num<0.25){
		num = num - 0.10;
		dimes = dimes + 1;
	}
	
	//subtract the nickels and count how many times it is subtracted.
	while(num>=0.5&& num<0.10){
		num = num - 0.5;
		nickels = nickels + 1;
	}

	// //subtract the pennies and count how many times it is subtracted.
	while(num<0.5 && num>0){
		num = num - 0.1;
		pennies = pennies + 1;
	}

	printf("Number of quarters: %d\n",quarters);
	printf("Number of dimes: %d\n",dimes);
	printf("Number of nickels: %d\n",nickels);
	printf("Number of pennies: %d\n",pennies);

	return  0;

}
```
## Exercise 6-5

A leap year is any year divisible by 4, unless the year is divisible by 100, but not 400. Write a program to tell if a year is a leap year
```c
#include  <stdio.h>
/*
A leap year is any year divisible by 4, unless the year is
divisible by 100, but not 400. Write a program to tell if a year 
is a leap year
*/

char line[100];
int year;
int main(void) {
	printf("Enter a year\n");
	fgets(line,sizeof(line),stdin);
	sscanf(line,"%d",&year);

	if(year%4 == 0 && (year%100 != 0 || year%400 == 0) ){
	printf("%d is a leap year",year);
	} else {
	printf("%d is not a leap year",year);
	}

	return  0;

}
```
## Exercise 6-6
Write a program that, given the number of hours an employee worked and the hourly wage, computes the employee's weekly pay. Count any hours over 40 as overtime at time and a half.
```c
#include  <stdio.h>
#include  <math.h>

/*
Program that, given the number of hours an employee worked and the
hourly wage, computes the employee's weekly pay. Count any hours
over 40 as overtime at time and a half.
*/

char line[100];
int hours_worked;
double hourly_wave;
double weekly_pay;
int extra_hours;

int main(void) {
printf("Enter the number of hours worked\n");
fgets(line, sizeof(line), stdin);
sscanf(line, "%d", &hours_worked);

printf("Enter the hourly wage\n");
printf("$");
fgets(line, sizeof(line), stdin);
sscanf(line, "%lf", &hourly_wave);

if(hours_worked > 40){
extra_hours = hours_worked - 40; //only de extra hours

//40 hours normal pay + overtime paid like an hour and a half
weekly_pay = ((40)*(hourly_wave))+
((extra_hours)*(pow(hourly_wave, 1.5)));.

} else {
weekly_pay = (hours_worked)*(hourly_wave); //Normal pay
}

printf("The weekly pay is: $ %lf",weekly_pay);

return  0;

}
```
## Exercise 6-7 Free program
Program that solves the quadratic equation ax2 + bx + c.
```c
#include  <stdio.h>
#include  <math.h>
/*
Program that solves the quadratic equation ax2 + bx + c.
*/

double a, b, c, d, e;

int main() {
printf("Program to calculate standard quadratic equation a*x^2 + b*x + c = 0\n");
printf ("Enter the value of a: ");
scanf ("%lf", &a);
  
printf ("Enter the value of b: ");
scanf ("%lf", &b);
  
printf ("Enter the value of c: ");
scanf ("%lf", &c);

d = pow(b,2) -(4 * a * c);

e = 2 * a;

if (d == 0){
printf ("The result is x1 = x2 =%lf", - b / e);
} else {
	if (d > 0) {
	printf ("The result is:\n");
	printf ("x1 = %lf \n", (-b + sqrt(d)) / e);
	printf ("x2 = %lf \n", (-b - sqrt(d)) / e);
	} else {
	printf ("The result is: \n");
	printf ("x1 = %lf + %lf * i \n", -b / e, sqrt(-d)/e);
	printf ("x2 = %lf - %lf * i \n", -b / e, sqrt(-d)/e);
	}	
}

return  0;

}
```
