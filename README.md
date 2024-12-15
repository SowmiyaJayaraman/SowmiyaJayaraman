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
