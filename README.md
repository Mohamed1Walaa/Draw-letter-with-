# Draw-letter-with-
# Letter Drawing Program in C

This program takes a character input from the user (A-Z) and displays its representation using a 2D array of asterisks `*`.

## Code

```c
#include <stdio.h>
#include <ctype.h>

int main() {
    char ch;
    char symbol = '*';

    printf("Enter a character (A-Z): ");
    scanf(" %c", &ch);
    ch = toupper(ch);

    if (ch == 'A') {
        
        int pattern[5][5] = {
            {0,1,0,1,0},
            {1,0,0,0,1},
            {1,1,1,1,1},
            {1,0,0,0,1},
            {1,0,0,0,1}
        };

        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 5; j++) {
                printf("%c", pattern[i][j] ? symbol : ' ');
            }
            printf("\n");
        }
    } else {
        printf("Character not supported yet.\n");
    }

    return 0;
}

