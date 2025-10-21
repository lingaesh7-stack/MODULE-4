# NAME : LINGAESHWAR K
# REGISTER NUMBER : 25016881

# MODULE-4
Module 4 respository for lab

---

# 1.Program: Find the Minimum of Three Numbers

**Aim:**  
To find and display the minimum of three numbers entered by the user using the conditional (ternary) operator.

**Algorithm:**  
1. Start the program.  
2. Declare three integer variables `n1`, `n2`, `n3` and a variable `min` to store the minimum.  
3. Read three numbers from the user.  
4. Use the ternary operator to compare the numbers:  
   - First, compare `n1` and `n2`.  
   - Then, compare the smaller of `n1` and `n2` with `n3`.  
5. Store the smallest number in `min`.  
6. Print the minimum number along with the input numbers.  
7. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int main()
{
    int n1, n2, n3, min;
    scanf("%d %d %d", &n1, &n2, &n3);

    min = (n1 < n2) ? ((n1 < n3) ? n1 : n3) : ((n2 < n3) ? n2 : n3);

    printf("Minimum between %d, %d and %d = %d", n1, n2, n3, min);
    return 0;
}
```
**output:**


<img width="774" height="192" alt="image" src="https://github.com/user-attachments/assets/209cbde6-9bc5-4658-a402-9764c6030387" />

**Result:**

The program successfully determines and displays the smallest of the three numbers entered by the user.
---

# 2.Program: Temperature Classification

**Aim:**  
To classify the weather based on the temperature entered by the user and display an appropriate message.

**Algorithm:**  
1. Start the program.  
2. Declare a variable `temp` to store the temperature.  
3. Read the temperature value from the user.  
4. Use conditional statements to check the temperature range and print the corresponding message:  
   - If `temp < 0` → "Freezing weather"  
   - If `0 ≤ temp ≤ 10` → "Cold weather"  
   - If `10 < temp < 20` → "Very Cold weather"  
   - If `20 ≤ temp ≤ 30` → "Normal in temp"  
   - If `30 < temp < 40` → "It's Hot"  
   - If `temp ≥ 40` → "It's very hot"  
5. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int main()
{
    float temp;
    scanf("%f", &temp);

    if (temp < 0)
        printf("Freezing weather.");
    else if (temp >= 0 && temp <= 10)
        printf("Cold weather.");
    else if (temp > 10 && temp < 20)
        printf("Very Cold weather.");
    else if (temp >= 20 && temp <= 30)
        printf("Normal in temp.");
    else if (temp > 30 && temp < 40)
        printf("It's Hot");
    else if (temp >= 40)
        printf("It's very hot.");

    return 0;
}
```
**output**

<img width="498" height="200" alt="image" src="https://github.com/user-attachments/assets/4ee36aaa-1c06-4df7-8e4d-3c9804c7e7cb" />

**Result:**

The program evaluates the entered temperature and displays a message describing the type of weather accordingly.
---


# 3. Program: Compare Two Strings

**Aim:**  
To compare two strings entered by the user and determine whether they are the same or different.

**Algorithm:**  
1. Start the program.  
2. Declare two character arrays `str1` and `str2` to store the input strings.  
3. Read both strings from the user.  
4. Call the function `compare(char a[], char b[])` to compare the strings:  
   - Initialize `flag = 0` and `i = 0`.  
   - Use a while loop to traverse both strings simultaneously until the null character `\0` is encountered.  
   - If any corresponding characters differ, set `flag = 1` and break the loop.  
5. The function returns `0` if strings are the same, otherwise `1`.  
6. In `main`, check the return value and display:  
   - "strings are same" if return value is `0`.  
   - "strings are not same" if return value is `1`.  
7. End the program.  

**Source Code:**  
```c
#include <stdio.h>  

int compare(char[], char[]);  

int main()  
{  
    char str1[20]; // declaration of char array  
    char str2[20]; // declaration of char array  
    
    scanf("%s", str1);  
    scanf("%s", str2);  
    
    int c = compare(str1, str2); // calling compare() function  
    
    if (c == 0)  
        printf("strings are same");  
    else  
        printf("strings are not same");  
    
    return 0;  
}  

// Function to compare both the strings  
int compare(char a[], char b[])  
{  
    int flag = 0, i = 0;  
    
    while (a[i] != '\0' && b[i] != '\0')  
    {  
        if (a[i] != b[i])  
        {  
            flag = 1;  
            break; 
        }  
        i++;  
    }  
    
    if (flag == 0)  
        return 0;  
    else  
        return 1;  
}  
```
**output**

<img width="570" height="201" alt="image" src="https://github.com/user-attachments/assets/c2a5de8b-7532-435d-b133-2c42bb4e522d" />

**Result:**

The program successfully compares the two input strings and displays whether they are the same or not.
---


# 4.Program: Count Spaces in a String

**Aim:**  
To count the number of words in a string entered by the user.

**Algorithm:**  
1. Start the program.  
2. Declare a character array `str[100]` to store the input string.  
3. Initialize a counter variable `count = 0`.  
4. Read the input string using `fgets()`.  
5. Traverse the string using a loop until the null character `\0` is encountered.  
6. For each character, check:  
   - If it is a space `' '` or newline `'\n'`, increment `count`.  
7. Optionally, handle cases where the string starts with a space or newline.  
8. Print the total count of spaces.  
9. End the program.  

**Source Code:**  
```c
#include <stdio.h>

int main()
{
    char str[100];
    int ind, count = 0;

    fgets(str, sizeof(str), stdin);

    for (ind = 0; str[ind] != '\0'; ind++) {
        if (str[ind] == ' ' || str[ind] == '\n') {
            count++;
        }
    }

    if (ind > 0 && (str[0] == ' ' || str[0] == '\n')) {
        count++;
    }

    printf("%d", count);
    return 0;
}
```
**output**

<img width="535" height="154" alt="image" src="https://github.com/user-attachments/assets/21be4b92-8f50-4231-ac9b-ce540398c62b" />

**Result:**

The program counts and displays the total number of words in the entered string.
---

# 5.Program: Convert a String to Uppercase

**Aim:**  
To convert all lowercase characters in a string to uppercase and display the result.

**Algorithm:**  
1. Start the program.  
2. Declare a character array `str[100]` to store the input string.  
3. Read the string from the user using `fgets()`.  
4. Traverse the string using a loop until the null character `\0` is encountered.  
5. For each character, use the `toupper()` function to convert it to uppercase.  
6. Replace the original character with the uppercase character in the string.  
7. Print the converted uppercase string.  
8. End the program.  

**Source Code:**  
```c
#include <stdio.h>
#include <ctype.h>

int main()
{
    char str[100];
    int i;

    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        str[i] = toupper(str[i]);
    }

    printf("%s", str);
    return 0;
}
```
**output**

<img width="956" height="154" alt="image" src="https://github.com/user-attachments/assets/23c8d4a6-1580-408c-bdd8-d12a206d1d80" />

**Result:**

The program converts all lowercase letters in the entered string to uppercase and displays the resulting string.
---

  
