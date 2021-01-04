# Debugging-with-GDB

Let’s use an example to understand it.
Below program we are giving a number count which divides a given number in given range.


//simple.c

#include<stdio.h>

int checkDivisible(int num,int startRange,int endRange)
{
        int count=0,i=0;
        for (i = startRange ; i <=endRange; i++)
        {
                if (num%i == 0)
                        count++;
        }
        return count;
}

int main()
{

        int number = 1000,count=0,startRange=0,endRange=10;
        count = checkDivisible(number,startRange,endRange);
        printf("Total no count which divide number[%d] in range:[%d] to [%d] are:%d",number,startRange,endRange,count);

        return 0;
}



Compile this program for debugging and start debugging.

$gcc –g –o simple simple.c
-g used for compile it in debugging mode.


NOW WE CAN START DEBUGGING:
