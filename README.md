#include <stdio.h>
#include <string.h>

// Function to ask and evaluate questions
void askQuestion(int questionNumber) {
    char answer1;
    switch (questionNumber) {
        case 1:
            printf("What does the \"printf \" function in C do?\n");
            printf("A)  Scans input from the user\n");
            printf("B)  Performs mathematical calculations\n");
            printf("C)  Prints output to the screen\n");
           
           
            scanf(" %c", &answer1); 
            if (answer1 == 'C' || answer1 == 'c') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is C) Prints output to the screen\n");
            }
            break;
        case 2:
            printf("Which symbol is used to indicate a single-line comment in C?\n");
            printf("A)  //\n");
            printf("B) /* */\n");
            printf("C)  #\n");
            
            
            scanf(" %c", &answer1); 
            if (answer1 == 'A' || answer1 == 'a') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is A) //\n");
            }
            break;
        
        case 3:
            printf("How do you declare a variable in C?\n");
            printf("A) variableName;\n");
            printf("B)  int variableName;\n");
            printf("C)  variableName = value;\n");
            
            
            scanf(" %c", &answer1); 
            if (answer1 == 'B' || answer1 == 'b') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is B) int variableName;\n");
            }
            break;
        
        case 4:
            printf("Which data type is used to store whole numbers in C?\n");
            printf("A) float\n");
            printf("B) double\n");
            printf("C) int\n");
           
            
            scanf(" %c", &answer1); 
            if (answer1 == 'C' || answer1 == 'c') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is C) int\n");
            }
            break;
        
        case 5:
            printf("What is the size of the \"char\" data type in C?\n");
            printf("A) 1 byte\n");
            printf("B) 2 bytes\n");
            printf("C) 4 bytes\n");
           
           
            scanf(" %c", &answer1); 
            if (answer1 == 'A' || answer1 == 'a') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is A) 1 byte\n");
            }
            break;
        
        case 6:
            printf("What is the result of the expression: 10 mod 3?\n");
            printf("A) 3\n");
            printf("B) 1\n");
            printf("C) 0\n");
           
            
            scanf(" %c", &answer1); 
            if (answer1 == 'B' || answer1 == 'b') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is B) 1\n");
            }
            break;
        
        case 7:
            printf("What is the purpose of the \"if\" statement in C?\n");
            printf("A)  Loop execution\n");
            printf("B) Function declaration\n");
            printf("C)  Conditional execution\n");
           
            
            scanf(" %c", &answer1); 
            if (answer1 == 'C' || answer1 == 'c') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is C)  Conditional execution.\n");
            }
            break;
        
        case 8:
            printf("Which loop is used when you want to execute a block of code at least once?\n");
            printf("A) for\n");
            printf("B) while\n");
            printf("C) do-while \n");
           
            
            scanf(" %c", &answer1); 
            if (answer1 == 'C' || answer1 == 'c') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is C) do-while.\n");
            }
            break;
        
        case 9:
            printf("What is the header file for input and output functions in C?\n");
            printf("A) stdlib.h\n");
            printf("B) math.h\n");
            printf("C)  stdio.h\n");
            
            
            scanf(" %c", &answer1); 
            if (answer1 == 'C' || answer1 == 'c') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is C) stdio.h.\n");
            }
            break;
        
        case 10:
            printf("How do you access the value of a variable using its memory address in C?\n");
            printf("A) variableName\n");
            printf("B) *variableName\n");
            printf("C) &variableName\n");
            
            
            scanf(" %c", &answer1); 
            if (answer1 == 'B' || answer1 == 'b') {
                printf("Correct!\n");
            } else {
                printf("Incorrect. The correct answer is B) *variableName.\n");
            }
            break;
        
        // Add more cases for additional questions
        
        default:
            printf("Invalid question number.\n");
            break;
    }
}

// Function to handle quiz initiation
void startQuiz() {
    char choice[10];

    printf("DO YOU WANT TO TAKE THE QUIZ (yes/no): ");
    scanf("%s", choice);

    if (strcmp(choice, "yes") == 0) {
        printf("Great, let's begin!\n");
        int questionNumber;
        do {
            printf("Choose a question to answer (1-10), or enter 0 to quit: ");
            scanf("%d", &questionNumber);

            if (questionNumber != 0) {
                askQuestion(questionNumber);
            }
        } while (questionNumber != 0);

        printf("Thank you for playing the quiz!\n");
    } else if (strcmp(choice, "no") == 0) {
        printf("Alright, maybe next time!\n");
    } else {
        printf("Invalid choice.\n");
    }
}

int main() {
    char name[20];

    printf("PLEASE STATE YOUR NAME: ");
    scanf("%s", name); 
    printf("Welcome To the quiz, %s!\n", name); 
    startQuiz(); // Call the function to handle the quiz

    return 0;
}
