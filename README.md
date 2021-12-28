#include<stdio.h>
#include<conio.h>
void main()
{
 struct cricket  { char name[20];
                         int teamno;
                        int player_no;
                        int no_of_runs;
                        int no_of_wicket;
                       };
 struct cricket t[20] ;
 int n,i,max,pos=0;
 clrscr();
 printf("\n how many teams:");
 scanf("%d",&n);
 printf("\n------------ Enter the player Details-------------------\n");
 for(i=0;i<n;i++)
 { printf("\n EnterThe Name:");
   fflush(stdin);
   gets(t[i].name);
   fflush(stdin);
   printf("\n Enter the team no :");
   scanf("%d",&t[i].teamno);
   printf("\n Enter the Player no :");
   scanf("%d",&t[i].player_no);
   printf("\n Enter no of runs :");
   scanf("%d",&t[i].no_of_runs);
   printf("\n Enter no of wicket:");
   scanf("%d",&t[i].no_of_wicket);
   printf("\n-------------------------------------------------------\n");
 }
 max=t[0].no_of_wicket;
 for(i=0;i<n;i++)
 {
   if(max<t[i].no_of_wicket)
   {   max=t[i].no_of_wicket;
         pos=i;
   }
 }
  printf("\n\n\n_____________Highest Wicket Takes_____________________\n");
   printf("\n\t Name:%s",t[pos].name);
   printf("\n\t team no :%d",t[pos].teamno);
   printf("\n\t Player no :%d",t[pos].player_no);
   printf("\n\t runs :%d",t[pos].no_of_runs);
   printf("\n\t wicket:%d",t[pos].no_of_wicket);
   printf("\n----------------------------------------------------------\n");
getch();
}
