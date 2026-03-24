# C_Module-6

# EXP NO: 6a) C PROGRAM TO FIND CHARACTER 'R' IS VOWEL OR CONSONANT USING POINTER.

# AIM:
To write a C program to find character 'R' is vowel or consonant using pointer.

# ALGORITHM:
1. Take the character from the user as an input using scanf function.
2. Assign the address of the character into the character pointer.
3. Using if condition, check whether the character is vowel or consonant.
4. Print according to the condition using printf function.

# PROGRAM:
```
#include<stdio.h>
int main()
{
    char ch;
    scanf("%c",&ch);
    char *ptr=&ch;
    if(*ptr=='A' || *ptr=='E' || *ptr=='I' || *ptr=='O' || *ptr=='U' || *ptr=='a' || *ptr=='e' || *ptr=='i' || *ptr=='o' || *ptr=='u')
    {
        printf("%c is vowel.",ch);
    }
    else printf("%c is consonant.",ch);
    return 0;
}
```

# OUTPUT:
<img width="1142" height="308" alt="image" src="https://github.com/user-attachments/assets/ae7f285e-7ca0-4c08-aaba-b1860426089b" />

# RESULT:
Thus, the program is verified successfully.

# EXP NO: 6b) C PROGRAM TO PRINT 'HELLO' USING MALLOC() AND FREE().

# AIM:
To write a C program to Print 'Hello' using malloc() and free() .

# ALGORITHM:
1. Use the header files #include<stdlib.h> and #include<string.h>.
2. Declare a string and allocate the memory using malloc().
3. Check if the string is NULL or not using if condition.
4. Copy the value "Hello" into the string using strcpy() and print it using printf function.
5. Free the space using free().
   
# PROGRAM:
```
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
    char *str=(char*)malloc(6*sizeof(char));
    if(str==NULL) return -1;
    strcpy(str,"Hello");
    printf("%s\n",str);
    free(str);
    return 0;
}
```

# OUTPUT:
<img width="1146" height="262" alt="image" src="https://github.com/user-attachments/assets/8bfba7d8-d4bb-4bbf-a618-c02c9f8f4c11" />

# RESULT:
Thus, the program is verified successfully.

# EXP NO: 6c) C PROGRAM TO PRINT THE VALUE OF THE WEDNESDAY USING ENUMERATION.
enum day {sunday, monday, tuesday, wednesday, thursday, friday, saturday};

# AIM:
To write a C program to print the value of the wednesday using enumeration.
enum day {sunday, monday, tuesday, wednesday, thursday, friday, saturday};

# ALGORITHM:
1. Use enum function and declare all the days in it.
2. Inside main() function, print the value of the wednesday using printf function.
3. Exit the program using return 0.
   
# PROGRAM:
```
#include<stdio.h>
enum day{sunday, monday, tuesday, wednesday, thursday, friday, saturday};
int main()
{
    printf("The day number stored in d is %d\n",wednesday+1);
    return 0;
}
```

# OUTPUT:
<img width="1148" height="275" alt="image" src="https://github.com/user-attachments/assets/da9ddf21-c71d-417a-91c3-86450b950b75" />

# RESULT:
Thus, the program is verified successfully.

# EXP NO: 6d) C PROGRAM TO ACCEPT DETAILS OF 'N' EMPLOYEE(ENO, ENAME, SALARY) AND DISPLAY THE DETAILS OF EMPLOYEE HAVING HIGHEST SALARY. USE ARRAY OF STRUCTURE.

# AIM:
To write a C program to accept details of 'n' employee(eno, ename, salary) and display the details of employee having highest salary. Use array of structure.

# ALGORITHM:
1. Define a structure.
2. Inside main() function, define the structure variable, and the n value.
3. Take the input of n value from the user using scanf function.
4. Using fo loop, take all the input values from the user using scanf function.
5. Inside the if condition, check whether the iterated salary is greater than the max salary.
6. If the condition is true, then the iterated salary will be equal to the max salary.
7. Print the given statement using printf function.
8. Again using for loop and if condition, check whether the iterated salary and the max salary are equal or not.
9. If they are equal, print the given statement using printf function.
    
# PROGRAM:
```
#include<stdio.h>
struct Employee
{
    int eno;
    char ename[50];
    float salary;
};
int main()
{
    struct Employee emp[100];
    int n,itr;
    float maxSalary=0;
    scanf("%d",&n);
    for(itr=0;itr<n;itr++)
    {
        scanf("%d %s %f",&emp[itr].eno,emp[itr].ename,&emp[itr].salary);
        if(emp[itr].salary>maxSalary)
        {
            maxSalary=emp[itr].salary;
        }
    }
        printf("Highest salary employee details:");
        for(itr=0;itr<n;itr++)
        {
            if(emp[itr].salary==maxSalary)
            {
                printf("%d      %s      %.0f",emp[itr].eno,emp[itr].ename,emp[itr].salary);
            }
        }
        return 0;
}
```

# OUTPUT:
<img width="1159" height="872" alt="image" src="https://github.com/user-attachments/assets/afe269b2-f08c-4164-a743-c2ef06bee5c4" />

# RESULT:
Thus, the program is verified successfully.

# EXP NO: 6e) C PROGRAM TO READ AND DISPLAY AN ARRAY OF N INTEGERS.

# AIM:
To write a C program to read and display an array of n integers.

# ALGORITHM:
1. Declare the size(n) and take it as an input from the user using scanf function.
2. Declare an integer array of size n.
3. Assign the address of the array into the integer pointer.
4. Using for loop, take the array elements as input from the user using scanf function.
5. Print the elements using printf function.

# PROGRAM:
```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int arr[n];
    int *ptr=arr;
    for(int itr=0;itr<n;itr++)
    {
        scanf("%d",ptr+itr);
        printf("the elements are %d\n",*(ptr+itr));
    }
    return 0;
}
```
OUTPUT:
<img width="1147" height="424" alt="image" src="https://github.com/user-attachments/assets/f940fe64-fd05-4fa9-aa58-7f9a826f0631" />

RESULT:
Thus, the program is verified successfully.

