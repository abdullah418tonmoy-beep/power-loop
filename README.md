#include <stdio.h>

int main()
{
    int base, exponent;
    int result = 1; 

  
    printf("Enter your base num: ");
    scanf("%d", &base);

 
    printf("Enter your exponent num: ");
    scanf("%d", &exponent);
       // ১. পাওয়ার মাইনাস হলেও লুপ চালানোর জন্য তাকে প্লাস (Absolute) বানিয়ে নেওয়া
    int abs_exponent = exponent < 0 ? -exponent : exponent;


    for(int i = 0; i < abs_exponent; i++)
    {
        result = result * base; 
    }
    if(exponent<0)
    {
        result= 1/result;
    }

  
    printf("Result is: %d\n", result);

    return 0;
}


