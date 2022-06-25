#bb
#include <stdio.h>
#include <math.h>
#include <stdlib.h>
float func(float x)
{
return (x*x*x-3*x-5);//Function f(x)
}
float funcd(float x)
{
return(3*x*x-3);//Differentiation of function f(x)
}
int main()
{
int pos=0, i=0;
float x, x0=0, x1=0, xi=0, fxi=0, fdxi=0,d;
while(1)
{
if(func(i)==0)
{
printf("Exact Root is found at x=%d",i);
}
if(func(i)*func(i+1)<0)
{
pos++;
break;
}
i++;
}
if(pos)
{
x0=i;
x1=i+1;
printf("Range of the given function is from %.0f to %.0f",x0,x1);
}
else
{
printf("Range of the given function NOT FOUND!!!\n");
}
if(pos)
{
x=x0;//x0 is Range here
printf("\n In Calculation table of Newton - Raphson Method \n");
xi=x-(func(x));//fund(x));//First iteration 
fxi=func(xi);//Putting value of xi in function f(x)
fdxi=funcd(xi);//Putting value of xi in function f’(x)
d=xi-x;
printf("\nIterations\t\txi\t\txi-xi+1\t\tfxi\t\tfdxi\n");
for(i=0;;i++)
{
printf("\n%d\t\t%.4f\t\t%.4f\t\t%.4f\t\t%.4f\n",i+1,xi,d,fxi,fdxi);
if((float)fabs(xi-x)<=.0001f || fabs(xi-x)<=.0001f)
{
break;
}
x=xi;
xi=x-(func(x)/funcd(x));//xi for next iteration
fxi=func(xi);
fdxi=funcd(xi);
d=xi-x;
}
}
printf("\n Root of the given function is %.4f\n",xi);
return 0;
}
