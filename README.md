# TIC-TAC-TOE
code
#include <stdio.h>

int main()
{
    char ttt[9] = {' ',' ',' ',' ',' ',' ',' ',' ',' '};
    char move = 'x';
    int pos;

    for(int i=1; i<=9; i++)
    {
        printf("Enter you move:");
        scanf("%d",&pos);

        ttt[pos] = move;

        printf("%c|%c|%c\n",ttt[0],ttt[1],ttt[2]);
        printf("-+-+-\n");
        printf("%c|%c|%c\n",ttt[3],ttt[4],ttt[5]);
        printf("-+-+-\n");
        printf("%c|%c|%c\n",ttt[6],ttt[7],ttt[8]);

        if(ttt[0]=='x' && ttt[1]=='x' && ttt[2]=='x' ||
           ttt[3]=='x' && ttt[4]=='x' && ttt[5]=='x' ||
           ttt[6]=='x' && ttt[7]=='x' && ttt[8]=='x' ||
           ttt[0]=='x' && ttt[3]=='x' && ttt[6]=='x' ||
           ttt[1]=='x' && ttt[4]=='x' && ttt[7]=='x' ||
           ttt[2]=='x' && ttt[5]=='x' && ttt[8]=='x' ||
           ttt[0]=='x' && ttt[4]=='x' && ttt[8]=='x' ||
           ttt[2]=='x' && ttt[4]=='x' && ttt[6]=='x')
        {
            printf("x wins,Game Over");
        }
        else if(ttt[0]=='o' && ttt[1]=='o' && ttt[2]=='o' ||
                ttt[3]=='o' && ttt[4]=='o' && ttt[5]=='o' ||
                ttt[6]=='o' && ttt[7]=='o' && ttt[8]=='o' ||
                ttt[0]=='o' && ttt[3]=='o' && ttt[6]=='o' ||
                ttt[1]=='o' && ttt[4]=='o' && ttt[7]=='o' ||
                ttt[2]=='o' && ttt[5]=='o' && ttt[8]=='o' ||
                ttt[0]=='o' && ttt[4]=='o' && ttt[8]=='o' ||
                ttt[2]=='o' && ttt[4]=='o' && ttt[6]=='o')
        {
            printf("o wins,Game Over");
        }
        else
        {
            printf("Tie");
        }

        if(move='x')
            move='o';
        else
            move='x';
    }

    return 0;
}

    
