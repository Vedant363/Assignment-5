# Assignment-5
Simple Calculator
#include<stdio.h>
int main()
{
int ch;
float a,b;
char q;
int base,exp,result,i,power=1,f=1,num;
do{
printf("           \t***************// CALCULATOR //*****************\n\n");
printf("\n=> For addition (+)                :press '1' ");
printf("\n=> For substraction (-)            :press '2' ");
printf("\n=> For multiplication (*)          :press '3' ");
printf("\n=> For division (/)                :press '4' ");
printf("\n=> For exponential function (x^y)  :press '5' ");
printf("\n=> For factorial number(x!)        :press '6' ");
scanf("%d",&ch);
if (ch>6)
{
  printf("\nError!! (Please follow the instructuions carefully)");
  return 0;
}
else if (ch<1)
{
  printf("\nError!! (Please follow the instructuions carefully)");
  return 0;
}
else if (ch<=4 && ch>=1)
{
printf("\n Enter the first number:");
scanf("%f",&a);
printf("\n Enter the second number:");
scanf("%f",&b);

switch(ch)
 {
case 1: printf("\n=> Addition of the numbers is:   %0.2f\n",a+b);
break;
case 2: printf("\n=> Subtraction of the numbers is :  %0.2f\n",a-b);
break;
case 3: printf("\n=> Multiplication of the numbers is :  %0.2f\n",a*b);
break;
case 4: if(b==0)
printf("\n Denominator cannot be zero");
else
printf("\n=> Division of the numbers is :  %0.3f\n",a/b);
break;
default:printf("\nERROR!!\n");
 }
 printf("\n Do you want to continue? (Press 'y' for YES/ 'n' for no)\n\n");
scanf(" %c",&q);
}
else if (ch==5)
{
switch(ch)
case 5: 
{
printf("\nEnter a base number(x): \n");
scanf("%d", &base);
printf("\nEnter an exponent(y): \n");
scanf("%d", &exp);
for(i=0;i<exp;i++)
 {
  power= power * base;
 }
printf("\nx^y => :   %d\n",power);
break;
default:printf("\nERROR!!\n");
}
printf("\n Do you want to continue? (Press 'y' for YES/ 'n' for no)\n\n");
scanf(" %c",&q);
 }
 else if (ch==6)
 {
  switch(ch)
  case 6:
  { 
  printf("\nEnter a number: \n");
  scanf("%d",&num);
 
  for(i=1;i<=num;i++)
      f=f*i;
     
  printf("Factorial of %d is: %d\n",num,f);
  break;
  default:printf("\nERROR!!\n");
 }
 printf("\n Do you want to continue? (Press 'y' for YES/ 'n' for no)\n\n");
scanf(" %c",&q);
 }

}while(q=='y');
}

