# PFC-LAB-RECORD
AIM 1
#include <stdio.h>

int main()
{
    // print name and age
   printf("hello, my name is Aastha sen.\n");
    printf("I am 19 years old.\n");
    return 0;// indicate successful program termination
}

AIM 2
#include <stdio.h>

int main() {
    int num1, num2, sum, largest;

    // input two numbers 
    printf("Enter the first number: ");
    scanf("%d" , &num1);
    printf("Enter the second number: ");
    scanf("%d ", &num2);

    //calculate the sum 
    sum = num1 + num2;
     
    //Determine the largest number
    if (num1 > num2){
        largest = num1;
    } else {
        largest = num2;
    }
//output the results
printf("The sum of %d and %d is : %d\n", num1, num2, sum);
printf("The largest of %d and %d is: %d\n, num1, num2, largest");

return 0;

}

AIM 3
#include <stdio.h>

int main(){
// Step 1: Declare variables
int intvar, temp;
float floatvar;
char charvar;
double doublevar;

// Step 2: Put values using scanf
printf("Enter an integer: ");
scanf("%d", &intvar);

printf("Enter a float: ");
scanf("%f", &floatvar);

printf("Enter a character: ");
scanf(" %c", &charvar); // Note the space before %c to handle newline issues

printf("Enter a double: ");
scanf("%lf", &doublevar);

// Step 3: Print values using printf
printf("\nYou entered:\n");
printf("Integer: %d\n", intvar);
printf("Float: %.2f\n", floatvar);
printf("Character: %c\n", charvar);
printf("Double: %.4lf\n", doublevar);

// Step 4: Swap two numbers (example: swapping intvar and temp)
printf("\nEnter another integer to swap with the first: ");
scanf("%d", &temp);

printf("\nBefore swapping: intvar = %d, temp = %d\n", intvar, temp);

// Swapping logic
intvar = intvar + temp;
temp = intvar - temp;
intvar = intvar - temp;

printf("After swapping: intvar = %d, temp = %d\n", intvar, temp);

return 0;
}

AIM 4
#include <stdio.h>

int main() {
    int choice;

    printf("\n----- MENU -----\n");
    printf("1. Check Odd or Even\n");
    printf("2. Maximum of Three Numbers (Nested if)\n");
    printf("3. Maximum of Two Numbers (Ternary Operator)\n");
    printf("4. Calculator using Switch Case\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);

    switch (choice) {

        case 1: {
            int num;
            printf("Enter a number: ");
            scanf("%d", &num);

            if (num % 2 == 0)
                printf("%d is Even", num);
            else
                printf("%d is Odd", num);
            break;
        }

        case 2: {
            int a, b, c;
            printf("Enter three numbers: ");
            scanf("%d %d %d", &a, &b, &c);

            if (a > b) {
                if (a > c)
                    printf("Maximum number is %d", a);
                else
                    printf("Maximum number is %d", c);
            } else {
                if (b > c)
                    printf("Maximum number is %d", b);
                else
                    printf("Maximum number is %d", c);
            }
            break;
        }

        case 3: {
            int x, y, max;
            printf("Enter two numbers: ");
            scanf("%d %d", &x, &y);

            max = (x > y) ? x : y;
            printf("Maximum number is %d", max);
            break;
        }

        case 4: {
            int op;
            float n1, n2;

            printf("\nCalculator Menu\n");
            printf("1. Addition\n2. Subtraction\n3. Multiplication\n4. Division\n");
            printf("Enter operation: ");
            scanf("%d", &op);

            printf("Enter two numbers: ");
            scanf("%f %f", &n1, &n2);

            switch (op) {
                case 1:
                    printf("Result = %.2f", n1 + n2);
                    break;
                case 2:
                    printf("Result = %.2f", n1 - n2);
                    break;
                case 3:
                    printf("Result = %.2f", n1 * n2);
                    break;
                case 4:
                    if (n2 != 0)
                        printf("Result = %.2f", n1 / n2);
                    else
                        printf("Division by zero not allowed");
                    break;
                default:
                    printf("Invalid operation");
            }
            break;
        }

        default:
            printf("Invalid choice");
    }

    return 0;
}

AIM 5
#include <stdio.h>
int main(){
    int n, sum=0;
    scanf("%d" , &n);
    for(int i =1; i<=n; i+=2){
        sum += i;
    }
    printf("odd sum = %d", sum);
    return 0;
    
}

AIM 6
#include <stdio.h>

int main(){
    int n, sum = 0;
    scanf("%d", &n);

    for(int i= 1; i<=n; i++){
        if (n % i == 0){
            sum += i;
        }
    }
    printf("Sum of divisor - %d", sum);
    return 0;
}

AIM 7
#include  <stdio.h>

int main (){
int n;
scanf("%d", &n);

for ( int i = 1; i<=10; i ++){
    printf("%d * %d = %d\n", n, 1, n*1);
}
return 0;

}

AIM 8
#include <stdio.h>

/* Function definition */
int square(int n) {
    return n * n;
}

int main() {
    int num, result;

    printf("Enter a number: ");
    scanf("%d", &num);

    result = square(num);   // Function call

    printf("Square of %d is %d", num, result);

    return 0;
}

AIM 9
#include <stdio.h>

/* Function using return */
int square_return(int n) {
    return n * n;   // returns value to main
}

/* Function using printf */
void square_print(int n) {
    printf("Square using printf = %d\n", n * n);
}

int main() {
    int num, result;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Using return */
    result = square_return(num);
    printf("Square using return = %d\n", result);

    /* Using printf */
    square_print(num);

    return 0;
}

AIM 10
#include <stdio.h>

/* Function to check prime number */
int isPrime(int n) {
    int i;

    if (n <= 1)
        return 0;

    for (i = 2; i <= n / 2; i++) {
        if (n % i == 0)
            return 0;
    }
    return 1;
}

/* Function to find factorial */
long long factorial(int n) {
    long long fact = 1;
    int i;

    for (i = 1; i <= n; i++) {
        fact = fact * i;
    }
    return fact;
}

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Prime number check */
    if (isPrime(num))
        printf("%d is a Prime number\n", num);
    else
        printf("%d is Not a Prime number\n", num);

    /* Factorial */
    if (num >= 0)
        printf("Factorial of %d is %lld", num, factorial(num));
    else
        printf("Factorial not defined for negative numbers");

    return 0;
}

AIM 11
#include <stdio.h>

/* Function to swap values using pass by reference */
void swap(int *a, int *b) {
    int temp;

    temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x, y;

    printf("Enter two numbers: ");
    scanf("%d %d", &x, &y);

    printf("Before swapping: x = %d, y = %d\n", x, y);

    swap(&x, &y);   // function call (address passed)

    printf("After swapping: x = %d, y = %d", x, y);

    return 0;
}
