

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>

int max_four_no(int a,int b,int c,int d)

{

    int max=a;

    if(b>max)
    {

        max=b;

    }

    if(c>max)
    {

        max =c;

    }

    if(d>max)
    {

        max=d;

    }

    return max;

}

int main()

{

    int a,b,c,d;

    scanf("%d%d%d%d",&a,&b,&c,&d);

    int ans = max_four_no(a,b,c,d);

    printf("%d",ans);

}
```

Output:

![437947775-77239f7a-64f5-4080-b9f7-608037d488c1](https://github.com/user-attachments/assets/e39d43a1-aaa2-4088-9370-65a7a159474d)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>
void calculate_the_max(int n, int k)
{
    int a = 0; // max AND
    int o = 0; // max OR
    int x = 0; // max XOR
    for (int i = 1; i <= n; i++) 
    {
        for (int j = i + 1; j <= n; j++)
        {
            int andV = i & j;
            int orV = i | j;
            int xorV = i ^ j;

        
        if (andV < k && andV > a) 
        {
            a = andV;
        }
        if (orV < k && orV > o)
        {
            o = orV;
        }
        if (xorV < k && xorV > x)
        {
            x = xorV;
        }
    }
}
printf("%d\n%d\n%d\n", a, o, x);
}
int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_max(n, k);
    return 0;
}
```

Output:

![437948051-386f281a-7a9f-498e-b14d-a4d84b1f9beb](https://github.com/user-attachments/assets/9415be5f-5e81-4acc-b9fb-e0f3b7e793e6)


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int noshel, noque;
    scanf("%d %d", &noshel, &noque);
    int *shelarr[1000];         
    int nobookarr[1000] = {0};  
    int k, c;   
    for (int i = 0; i < noshel; i++)
    {
        shelarr[i] = NULL;
    }
    for (int i = 0; i < noque; i++)
    {
        int queryType, x, y;
        scanf("%d", &queryType);
        if (queryType == 1)
        {
            scanf("%d %d", &x, &y);
            shelarr[x] = realloc(shelarr[x], (nobookarr[x] + 1) * sizeof(int));
            shelarr[x][nobookarr[x]] = y;
            nobookarr[x]++;
        } 
        else if (queryType == 2)
        {
            scanf("%d %d", &x, &y);
            printf("%d\n", shelarr[x][y]);
        }
        else if (queryType == 3)
        {
            scanf("%d", &x);
            printf("%d\n", nobookarr[x]);
        }
    }
    for (int i = 0; i < noshel; i++) {
    free(shelarr[i]);
   }

   return 0;
}
```

Output:

![437948369-17a555c9-417d-495c-9fcc-403f3e0ec898](https://github.com/user-attachments/assets/03b9a7f4-0e40-4982-ba49-dfa371b332c1)



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include<stdio.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    int arr[n];
    for(int i=0;i<n;i++)
    {
         scanf("%d",&arr[i]);
    }
    for(int i=0;i<n;i++)
    {
        sum+=arr[i];
    }
    printf("%d",sum);
}
```

Output:

![437948540-5aeb20eb-fd55-49b7-bdaf-1f8f465cadd8](https://github.com/user-attachments/assets/c29fcd6f-6bfd-4b04-a491-c6d408cdf452)


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
#include <ctype.h>

int main() 
{
    char sentence[1000];
    printf("Enter a sentence:\n");
    fgets(sentence, sizeof(sentence), stdin);
    int wordCount = 0;
    int inWord = 0; 
    for (int i = 0; sentence[i] != '\0'; i++)
    {
         if (!isspace(sentence[i]) && !ispunct(sentence[i]))
         {
              if (inWord == 0)
              {
                  wordCount++;
                  inWord = 1;
              }
          } 
          else
          {
              inWord = 0;
           }
    }
    printf("Total number of words: %d\n", wordCount);

    return 0;
}
```

Output:

![437948824-e437c9a7-c452-47b5-8012-bcdbba3cf345](https://github.com/user-attachments/assets/88ee558f-1ae9-4db4-8343-24248ce6dd4b)



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
