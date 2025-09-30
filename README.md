# Student-marks-calculator-
To calculate marks and percentage of the students
#include <stdio.h>

struct Student {
    char name[50];
    int marks[3];   // marks for 3 subjects
    int total;
    float percent;
};

int main() {
    struct Student s;
    int i;

    // Input
    printf("Enter student name: ");
    scanf("%s", s.name);

    s.total = 0;
    for(i = 0; i < 3; i++) {
        printf("Enter marks for subject %d: ", i+1);
        scanf("%d", &s.marks[i]);
        s.total += s.marks[i];
    }

    s.percent = s.total / 3.0;

    // Output
    printf("\n--- Student Report ---\n");
    printf("Name      : %s\n", s.name);
    printf("Total     : %d\n", s.total);
    printf("Percentage: %.2f\n", s.percent);

    return 0;
}
