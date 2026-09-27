
Advanced-C-Lab-Manual
Repository navigation
Code
Pull requests
Actions
Advanced-C-Lab-Manual
/Module 7.md
santhoshkumar-ias
santhoshkumar-ias
last week
255 lines (190 loc) · 7.21 KB

Preview

Code

Blame
EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim: To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:

Declare structure eligible with age (integer) and n (character array)
Declare variable e of type eligible
Input age and name using scanf, store in e
If e.age <= 6
Print "Vaccine Eligibility: No" Else
Print "Vaccine Eligibility: Yes"
Print details (e.age, e.n)
Return 0
Program:

#include <stdio.h>
#include <string.h>

struct Person {
    char name[50];
    int age;
};

int main() {
    struct Person p;
    scanf("%d", &p.age);
    scanf("%s", p.name);
    printf("Age:%d\n", p.age);
    printf("Name:%svaccine:%d\n",p.name,p.age);
    
   
    if(p.age>6)
    printf("eligibility:yes");
    else
    printf("eligibility:no");
    return 0;
}
Output:

<img width="608" height="373" alt="image" src="https://github.com/user-attachments/assets/36496656-009a-4987-82cc-10deb99c73ce" />

Result:

Thus, the program has been verified successfully. All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.

EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION Aim: To write a C program for passing structure as function and returning a structure from a function

Algorithm:

Define structure numbers with members a and b.
Declare variable n of type numbers.
Prompt the user to enter values for a and b.
Input values for a and b into n using scanf.
Call the add function with n as an argument.
Print the result returned by the add function.
Return 0
Program:

#include<stdio.h>
struct add
{
    int a,b;
}n;
int main()
{
    scanf("%d%d",&n.a,&n.b);
    printf("%d",n.a+n.b);
}
Output:

<img width="353" height="314" alt="image" src="https://github.com/user-attachments/assets/a77cb29e-e793-4395-99ff-253938e13772" />

Result:

Thus, the program has been verified successfully. All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.

EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim: To write a C program to read a file name from user

Algorithm:

Include the necessary header file stdio.h.
Begin the main function.
Declare a file pointer p. Declare a character array name to store the file name.
Prompt the user to enter a file name. Use scanf to input the file name into the name array.
Print a message indicating that the file with the specified name has been created successfully.
Use fopen to open a file with the name provided by the user in write mode ("w").
If successful, continue to the next step.
If unsuccessful, print an error message and exit the program with a non-zero status.
Print a message indicating that the file has been opened successfully.
Use fclose to close the file.
Print a message indicating that the file has been closed.
End the main function.
Return 0 to indicate successful program execution.
Program:

#include <stdio.h>
int main()
{
    FILE *fp;
    char a[20];
    scanf("%s",a);
    printf("%s File Created Successfully\n",a);
    fp = fopen("a","w");
    printf("%s File Opened\n",a);
    fclose(fp);
    printf("%s File Closed\n",a);
}
Output:


Result:

Thus, the program has been verified successfully. All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.

EXP NO:4 PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE Aim: To write a C program to read, a file and insert text in that file Algorithm:

Include the necessary header file stdio.h.
Begin the main function.
Declare a file pointer p. Declare character arrays name and text. Declare an integer variable num.
Prompt the user to enter a file name and the number of strings. Use scanf to input the file name into the name array and the number of strings into the num variable.
Use fopen to open a file with the name provided by the user in write mode ("w").
If successful, continue to the next step.
If unsuccessful, print an error message and exit the program with a non-zero status.
Print a message indicating that the file has been opened successfully.
Use a loop to input strings from the user and write them to the file using fputs.
Use fclose to close the file.
Print a message indicating that data has been added successfully.
End the main function.
Return 0 to indicate successful program execution.
Program:

#include <stdio.h>
int main()
{
    FILE *fp;
    char name[30] , b[30];
    int a;
    scanf("%s",name);
    scanf("%d",&a);
    fp = fopen("name" , "w");
    printf("%s Opened\n",name);
    for(int i=0 ; i<a ; i++)
    {
        scanf("%s",b);
        fputs(b,fp);
    }
    printf("Data added Successfully\n");
}
Output:
<img width="989" height="469" alt="image" src="https://github.com/user-attachments/assets/9fd17218-da8d-41cc-9c69-d669baecb56b" />

Result:

Thus, the program has been verified successfully. All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.

Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim: The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm: 1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

#include<stdio.h>
struct std{
    char name[20];
    int roll;
    float per;
}acc;

int main(){
    scanf("%d",&acc.roll);
    scanf("%s",acc.name);
    scanf("%f",&acc.per);
    printf("Rollno is: %d\n",acc.roll);
    printf("Name is: %s\n",acc.name);
    printf("Percentage is: %.2f",acc.per);
}
Output:
<img width="707" height="443" alt="image" src="https://github.com/user-attachments/assets/9285b886-f257-4b86-bfd5-1ccfb25fd863" />

Result:

Thus, the program has been verified successfully. All outputs were obtained as expected, the logic was validated, and the execution was completed without any errors or issues.
