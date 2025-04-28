EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```
#include<stdio.h>
int main(){
    int num;
    scanf("%d",&num);
    switch(num){
        case 71:
        printf("seventy one");
        break;
        case 72:
        printf("seventy two");
        break;
        case 73:
        printf("seventy three");
        break;
        case 74:
        printf("seventy four");
        break;
         case 75:
        printf("seventy five");
        break;
         case 76:
        printf("seventy six");
        break;
         case 77:
        printf("seventy seven");
        break;
         case 78:
        printf("seventy eight");
        break;
         case 79:
        printf("seventy nine");
        break;
         default:
        printf("Greater than 79");
        break;
    }
   return 0;
}


```

Output:


![image](https://github.com/user-attachments/assets/5f43f372-93cc-4b12-96be-a67a1eb248ba)







Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include<stdio.h>
#include<string.h>
int  main(){
char s[20];
int i, a[10]={0};
scanf("%[^\n]",s);
for(i=0;i<strlen(s);i++){
    if(s[i]>='0'&&s[i]<='9'){
        a[s[i]-'0']++;
    }
}
    for(i=0;i<10;i++){
        printf("%d ",a[i]);
    }

    return 0;
}




```

Output:


![image](https://github.com/user-attachments/assets/7f7bbba9-c794-42e3-9f43-4a2f7c676ed5)







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int o(int n,char **s){
    int k=-1,i,l=1,j;
    for(i=0;i<n-1;i++){
        if(strcmp(s[i],s[i+1])<0)
        k=i;
    }
    if(k==-1) return 0;
    for(i=k+1;i<n;i++){
        if(strcmp(s[k],s[i])<0)
        l=i;
    }
    char *tmp=s[k];
    s[k]=s[l];
    s[l]=tmp;
    i=k+1,j=n-1;
    while(i<j){
        tmp=s[i];
        s[i++]=s[j];
        s[j--]=tmp;
    }
    return 1;
}
int main(){
    char **s;
    int n,i;
    scanf("%d",&n);
    s=calloc(n,sizeof(char*));
    for(i=0;i<n;i++){
        s[i]=calloc(11,sizeof(char));
        scanf("%s",s[i]);
    }
    do{
        for(i=0;i<n;i++){
            printf("%s%c",s[i],i==n-1?'\n':' ');
        }
    }while(o(n,s)); 
    for(i=0;i<n;i++){
        free(s[i]);
    }free(s);
    return 0;
}
```




Output:


![image](https://github.com/user-attachments/assets/ebb118c0-923e-4a33-bd53-59e4018c5f46)







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

void check(int i, int j, int first, int last, int n) {
  if(n >=1 )
  {
    if (i == first || i == last || j == first || j == last)
        printf("%d ", n);
    else
        check(i, j, first + 1, last - 1, n - 1);
  }
}

int main() 
{
    int n;
    scanf("%d", &n);
    int rows = 2 * n - 1;

    for (int i = 0; i < rows; i ++) {
        for (int j = 0; j < rows; j ++) {
            check(i, j, 0, rows - 1, n);
        }
        printf("\n");
    }
    return 0;
}
```




Output:


![image](https://github.com/user-attachments/assets/dccf6aa9-589c-47f8-9443-0061a864eb8d)






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

```
#include <stdio.h>

int getNumberFromUser() {
    int num;
   
    scanf("%d", &num);
    return num;
}

float calculateSquare(int n) {
    return (float)n * n;
}

int main() {
    int number = getNumberFromUser();
    float square = calculateSquare(number);

    printf("The square of %d is : %.2f\n", number, square);
    return 0;
}


```




Output:



![image](https://github.com/user-attachments/assets/7e6369b7-69c6-437a-9680-72d2754cbb96)






Result:
Thus, the program is verified successfully



























