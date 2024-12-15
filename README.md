//You are developing a memory management system for a game. The game stores player scores in an array where even-indexed positions represent one team and odd-indexed positions represent the other. For a special game mode, you need to swap the scores of the two teams stored in alternate indices.

For example, if the array of scores is: arr[] = {12, 4, 5, 1, 13, 9, 54, 34),

it should be rearranged to: arr[] = {4, 12, 1, 5, 9, 13, 34, 54).

Write a C program to interchange the odd-indexed and even-indexed elements in the array to implement this functionality.//
***********************-************
#include<stdio.h>
int main()
{
 int arr[]={1,2,3,4,5,6};
 int i, temp;
 for( i = 0 ; i <= 5 ; i = i + 2 )
{
   temp=arr[i];
   arr[i]=arr [i + 2] ;
   arr [i + 2] = temp;
}
 for( i = 0 ; i <= 5 ;i++)
   {
     printf("%d\n", arr[i]);
   }
     return 0;
}
****************************
output:
3
2
5
4
1
6
