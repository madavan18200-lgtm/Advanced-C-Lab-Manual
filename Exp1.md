EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include <stdio.h>

struct Person {
    char name[50];
    int age;
};

int main() {
    struct Person p[5];
    int i, n;

    printf("Enter number of persons: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("\nEnter name: ");
        scanf("%s", p[i].name);

        printf("Enter age: ");
        scanf("%d", &p[i].age);
    }

    printf("\n--- Vaccine Eligibility ---\n");

    for (i = 0; i < n; i++) {
        printf("%s (%d years): ", p[i].name, p[i].age);

        if (p[i].age > 6)
            printf("Eligible for vaccine\n");
        else
            printf("Not Eligible for vaccine\n");
    }

    return 0;
}
```
Output:

<img width="568" height="134" alt="image" src="https://github.com/user-attachments/assets/bd763cb3-6f2f-404d-b928-18d4d3177526" />


Result:
Thus, the program is verified successfully.
