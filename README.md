    #include <stdio.h>


    int main() {
    int n, i;
    float maths, physics, chemistry, english, cs;
    float total, average;
    char grade;

    printf("Enter number of students: ");
    scanf("%d", &n);


    for (i = 1; i <= n; i++) {


    printf("\nEnter marks of Student %d:\n", i);

    printf("Maths: ");
        scanf("%f", &maths);


     printf("Physics: ");
        scanf("%f", &physics);


    printf("Chemistry: ");
        scanf("%f", &chemistry);


    printf("English: ");
        scanf("%f", &english);


    printf("Computer Science: ");
        scanf("%f", &cs);


    total = maths + physics + chemistry + english + cs;
        average = total / 5;

    if (average >= 90) {
            grade = 'A';
        } 
        else if (average >= 80) {
            grade = 'B';
        }
        else if (average >= 70) {
            grade = 'C';
        }
        else if (average >= 60) {
            grade = 'D';
        }
        else if (average >= 50) {
            grade = 'E';
        }
        else {
            grade = 'F';
        }


    printf("\n--- Result of Student %d ---\n", i);
        printf("Total Marks : %.2f\n", total);
        printf("Average     : %.2f\n", average);
        printf("Grade       : %c\n", grade);
    }


    return 0;
    }
