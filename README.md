#include <stdio.h>

char calculateGrade(float average) {
    if (average >= 90) return 'A';
    else if (average >= 80) return 'B';
    else if (average >= 70) return 'C';
    else if (average >= 60) return 'D';
    else if (average >= 50) return 'E';
    else return 'F'; // Fail
}

int main() {
    int n, i;
    float maths, physics, chemistry, english, cs;
    float total, average;
    char grade;

    printf("Enter the number of students: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        printf("\nEnter marks for Student %d:\n", i);

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
        average = total / 5.0;
        grade = calculateGrade(average);

        printf("\n--- Result for Student %d ---\n", i);
        printf("Total Marks: %.2f\n", total);
        printf("Average Marks: %.2f\n", average);
        printf("Grade: %c\n", grade);
    }

    return 0;
}
