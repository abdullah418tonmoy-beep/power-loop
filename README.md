#include <stdio.h>

int main() {
    double base;
    int exponent;
    double result = 1.0;


    printf("Enter base (x): ");
    scanf("%lf", &base);
    printf("Enter integer exponent (y): ");
    scanf("%d", &exponent);

      //  পাওয়ার মাইনাস হলেও লুপ চালানোর জন্য তাকে প্লাস (Absolute) বানিয়ে নেওয়া
    int abs_exponent = exponent < 0 ? -exponent : exponent;


    for (int i = 0; i < abs_exponent; i++) {
        result *= base;
    }


    if (exponent < 0) {
        result = 1.0 / result;
    }


    printf("%.2lf^%d = %.6lf\n", base, exponent, result);

    return 0;
}
