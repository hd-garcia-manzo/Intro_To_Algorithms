# Exercise Functions 1

## Exercise 1
Create a function that receives a string and print the inverted string, remember that to print an element i you can use printf("%c",string[i]);
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
## Exercise 2
create a function that returns 0 if both have the same length and 1 if is different.
```c
#include  <stdio.h>
#include  <string.h>

int SameLenght (char string1[30], char string2[30]){

if (strlen(string1) == strlen(string2)){
return  0;
} else{
return  1;
}
}

char line1[30];
char line2[30];

int main(void) {

printf("Enter the first string\n");
fgets(line1, sizeof(line1), stdin);

printf("Enter the second string\n");
fgets(line2, sizeof(line2), stdin);

printf("1: Different Lenght\n");
printf("0: Same Lenght\n");

printf("Your strings have: %d \n",SameLenght(line1,line2));  

return  0;
}
```
## Exercise 3
create a function that returns 0 if both strings have the same elements, and when there's a different element. returns the first different char... an example: "var1X" and "var1Y", returns "X"
```c
#include  <stdio.h>
#include  <string.h>
  
char SameElements (char string1[30], char string2[30]){

char x;
char c;

for(int i = 0;i<strlen(string1); i++){
if(string1[i] != string2[i]){
c = string1[i];
break;
}

if(string1[i] == string2[i]) {
c = '0';
}
}

return c;

}

char line1[30];
char line2[30];

int main(void) {
  
printf("Enter the first string\n");
fgets(line1, sizeof(line1), stdin);

printf("Enter the second string\n");
fgets(line2, sizeof(line2), stdin);

printf("%c \n",SameElements(line1,line2));

return  0;

}
```
## Exercise 4
create a function where you insert a string and return 1 if is palindromic or not, it means that returns 1 if is palindrome ("ala"), return 0 if is not ("hello")
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
## Exercise 5
create a function where you enter a string of 30 chars and print only the consonants
```c
#include  <string.h>

int OnlyConsonants (char string[30]){
int x = strlen(string);
 
for(int i=0; i<x;i++){
if(string[i] != 'a' && string[i] != 'e' && string[i] != 'i' && string[i] != 'o'&& string[i] != 'u'){
printf("%c", string[i]);
}
} 

return  0;
}

int main(void) {
OnlyConsonants("Soloconsonantes");

return  0;

}
```
