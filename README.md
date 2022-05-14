# bb

# Write a c program to calculate factorial of a number using recursion.
*
#include<stdio.h>
long int mnum(int n);
int main() {
    int n;
    printf("Enter a positive integer: ");
    scanf("%d",&n);
    printf("Factorial of %d = %ld", n, mnum(n));
    return 0;
}

long int mnum(int n) {
    if (n>=1)
        return n*mnum(n-1);
    else
        return 1;
}
*









Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement:Write a c program to compute power of a given number using recursion.

Formula:
a^b=a*a*a…(b times)

Source code:
#include <stdio.h>
int pow(int b,int e){
  if(e==0){
    return 1;
  }else if(e==1){
    return b;
  }else{
    return b*pow(b,e-1);
  }
}
int main(){
  int b,e;
  printf("enter base and exponent ");
  scanf("%d %d",&b,&e);
  printf("result= %d",pow(b,e));
  return 0;
}





Output:
















Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement:Write a c program to calculate roots of quadratic equation of the form ax^2+bx+c=0 by calculating discriminant(d).

Formula:
d=b^2-4ac
roots=(-b +- sqrt(d))/2a

Source code:
#include <stdio.h>
#include <math.h>
void equal(int a, int b){
  float r=(-1*b)/(2.0*a);
  printf("\n%.3f",r);
}  
voiddistinct(int a,intb,int d){
  float r1=(-1*b+sqrt(d))/(2.0*a);
  float r2=(-1*b-sqrt(d))/(2.0*a);
  printf("\nr1 is %.3f and r2 is %.3f",r1,r2);
}
int main(){
  int a,b,c,d;
  printf("enter value for a,b and c in ax^2+bx^1+c:");
  scanf("%d %d %d",&a,&b,&c);
  d=(b*b)-(4*a*c);
  if(d>0){
    printf("\nreal and distinct roots");
    distinct(a,b,d);
  }else if(d==0){
    printf("\nreal and equal roots");
    equal(a,b);
  }else if(d<0){
    printf("\ncomplex roots");
  }
  return 0;
}


























Output:













Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement:Write a c program to create a mathematical operation with following operation
Addition, subtraction, multiplication and division
Square root
Power
Log

Formula:
Addition(+), subtraction(-), multiplication(*), division(/)
Square root(sqrt(number))
Power(pow(base, exponent))
Log(log(number))

Source Code:
#include <stdio.h>
#include <math.h>
int main(){
  int a,b,ch;
  while(1){
    printf("\n0-exit\n1-add\n2-sub\n3-multi\n4-div\n5-sqrt\n6-pow\n7-log\n\nchoice:");    
    scanf("%d",&ch);
    switch(ch){
      case 0:
        return 0;
      case 1:
        printf("\nenter a and b:");
        scanf("%d%d",&a,&b);
        printf("%d",a+b);
        break;
       case 2:
        printf("\nenter a and b:");
        scanf("%d%d",&a,&b);
        printf("%d",a-b);
        break;
       case 3:
        printf("\nenter a and b:");
        scanf("%d%d",&a,&b);
        printf("%d",a*b);
        break;
       case 4:
        printf("\nenter a and b:");
        scanf("%d%d",&a,&b);
        if(b==0){printf("\nerror");
          break;
        }
        printf("%d",a/b);
        break;
       case 5:
        printf("\nenter a:");
        scanf("%d",&a);
        printf("%.3f",sqrt(a));
        break;
       case 6:
        printf("\nenter a and b:");
        scanf("%d%d",&a,&b);
        printf("%.1f",pow(a,b));
        break;
       case 7:
        printf("\nenter a:");
        scanf("%d",&a);
        printf("%.3f",log(a));
        break;
       default:
         printf("\nwrong choice");
    }
  }  
}






Output:













Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement:Write a c program to calculate e^x series up to given number of terms. Then print sum of them.

Formula:
e^x = 1 + (x^1)/1! + (x^2)/2! + (x^3)/3! + …..(x^n)/n!

Source code:
#include <stdio.h>
#include <math.h>
int fact(int n){
  if(n==1 || n==0){
    return 1;
  }else{
    return n*fact(n-1);
  } 
}
int main(){
  int x;
  float s=0.0;
  printf("x=");
  scanf("%d",&x);
  for(int i=0;i<=8;i++){		//we have taken value of n=8
    s=s+(pow(x,i)/fact(i));
  }
  printf("result=%f",s);
  return 0;
}





Output:














Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102


Problem statement:Write a c program to compute absolute, relative and percentage error.

Formula:
Ea=|true value – approx value|
Er=Ea/true value
Ep=Er*100

Source code:
#include <stdio.h>
int main()
{
  double x,y;
  printf("enter accurate value:");
  scanf("%lf",&x);
  printf("enter approx value:");
  scanf("%lf",&y);
  double ea,er,ep;
  if(x>=y){
    ea=x-y;
  }else{
    ea=y-x;
  }
  er=ea/x;
  ep=er*100;
  printf("absolute error= %lf\nrelative error= %lf\npercentage error= %lf",ea,er,ep);
  return 0;
}



Output:












Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement: Find the root of the equation x^3-x-1=0 using bisection method.

Formula:
x=(a+b)/2

Source code:
#include<stdio.h>
#include<math.h>
float fuction(float x){
    return(pow(x,3)-x-1);		//given equation
}
int main(){
    int i=0;
    float a=0,b=1,x;
    if(fuction(a)==0){
        printf("root of the equation is %.4f",a);
        return 0;
    }else if(fuction(b)==0){
        printf("root of the equation is %.4f",b);
        return 0;
    }else{
        while((fuction(a)*fuction(b))>=0){		//product of two consecutive values should be -ve
            a++;
            b++;
        }
        printf("range of the equation is from %.4f to %.4f\n",a,b);
        printf("\nitr\ta\tb\tx\tf(x)\n\n");
        while(1){
            i++;
            x=(a+b)/2.0;		//mid point of the range
            if(fuction(x)==0.0 || (b-a)<=0.0001){
                break;		//when f(x) is 0 or difference b/w a and b is less than or equal to 0.0001
            }
            printf("%d\t%.4f\t%.4f\t%.4f\t%.4f\n",i,a,b,x,fuction(x));
            if(fuction(x)>0){
                b=x;		//if f(x) is +ve change b
            }else if(fuction(x)<0){
                a=x;		//if f(x) is -ve change a
            }
        }
        printf("root of the equation is %.4f",x);
        return 0;
    }
}




















Output:














Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102


Problem statement: Find the root of the equation x^3-17=0 using regular-falsi method.

Formula:
x2=x1-(f(x1)*(x1-x0))/(f(x1)-f(x0))

Source code:
#include<stdio.h>
#include<math.h>
float fuction(float x){
    return(pow(x,3)-17);		//given equation
}
int main(){
    int i=0;
    float x0=0.0,x1=1.0,x2;
    if(fuction(x0)==0){
        printf("root of the equation is %.4f",x0);
        return 0;
    }else if(fuction(x1)==0){
        printf("root of the equation is %.4f",x1);
        return 0;
    }else{
        while((fuction(x0)*fuction(x1))>=0){		//product of two consecutive values should be -ve
            x0++;
            x1++;
        }
        printf("range of the equation is from %.4f to %.4f\n",x0,x1);
        printf("\nitr\tx0\tx1\tx2\tf(x2)\n\n");
        while(1){
            i++;
            x2=x1-(fuction(x1)*(x1-x0))/(fuction(x1)-fuction(x0));		//formula
            if(fuction(x2)==0.0000 || (x1-x0)<=0.0001){
                break;		//when f(x2) is 0 of difference b/w x1 and x2 is less than 0.0001
            }
            printf("%d\t%.4f\t%.4f\t%.4f\t%.4f\n",i,x0,x1,x2,fuction(x2));
            if(fuction(x2)>0){
                x1=x2;		//if x2 is +ve change x1
            }else if(fuction(x2)<0){
                x0=x2;		//if x1 is -ve change x0
            }
        }
        printf("root of the equation is %.4f",x2);
        return 0;
    }
}



















Output:













Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement: Find root of the equation x=17^(1/3) using Newton Raphson method.

Formula:
xn=xn-1-f(xn-1)/f’(xn-1).

Source code:
#include<stdio.h>
#include<math.h>
float f(float x){
    return pow(x,3)-17;		//given equation
}
float df(float x){
    return 3*pow(x,2);		//derivative of the equation
}
float xn(float x){
    return x-f(x)/df(x);		//formula
}
int main(){
    float x0=0,x1=1,n,m,c;
    int i=1;
    if(f(x0)==0){
        printf("root of the equation is %.4f",x0);
        return 0;
    }else if(f(x1)==0){
        printf("root of the equation is %.4f",x1);
        return 0;
    }
    while (f(x0)*f(x1)>=0){		//product of two consecutive value should be -ve
        x0++;
        x1++;
    }
    m=x0;
    n=xn(m);
    printf("range of the equation is from %.4f to %.4f\n",x0,x1);
    printf("itr\txn\t\txn-xm\tf(xn)\tf\'(xn)\n\n");
    printf("%d\t%.4f\t\t\t%.4f\t%.4f\n",i,x0,f(x0),df(x0));
    i++;
    while(1){
        printf("%d\t%.4f\t%.4f\t%.4f\t%.4f\n",i++,n,n-m,f(n),df(n));
        if(n-m<0){		//if difference is -ve
            c=(-1)*(n-m);		//make it +ve by multiplying -1
            if(c<0.0001){            //check if difference is less than 0.0001
            printf("\n\nroot of the equation is %.4f",n);
            break;
            }
        }
        m=n;
        n=xn(m);
    }
}

















Output:














Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement: Find root of the equation x+sin(x)+1=0 using iteration method.

Formula:
xn=f’(xn-1)

Source code:
#include<stdio.h>
#include<stdlib.h>
#include<math.h>
float f(float x){
    return cos(x)-3*x+1;        //given equation
}
float f2(float x){
    return (cos(x)+1)/3.0;      //value of x from given equation
}
void conv(int x0,int x1){
    float a,b;
    int count=0;
    for(int i=0;i<2;i++){
        a=rand()%(x1-x0+1)+x0;      //generates random number b/w the range
        b=-sin(a)/3;        //derivative of original equation
        if(b<0){
            b=-1*b;
            if(b<1){
                count++;
            }
        }
    }
    if(count!=0){
        printf("\nas the iterative method is converging, we can apply iterative method.\n");
    }else{
        printf("\nwe cannot apply iterative method for this equation\n");
        exit(0);
    }
}
int main(){
    float x0=0.0,x1=1.0,xn,xm;
    int i=0;
    if(f(x0)==0.0){
        printf("root of the equation is %.4f",x0);
        return 0;
    }else if(f(x1)==0.0){
        printf("root of the equation is %.4f",x1);
        return 0;
    }
    while(f(x0)*f(x1)>=0){      //condition to find range
        x0++;
        x1++;
    }
    printf("range of the equation is from %.1f to %.1f",x0,x1);
    conv(x0,x1);
    xm=(x0+x1)/2;       //mid point of the range
    printf("itr\t  xn \txn - xn-1\n\n");
    while(1){
        xn=f2(xm);
        printf("%d\t%.4f\t%.4f\n",i,xn,xn-xm);
        if((xn-xm)>-0.0001 & (xn-xm)<0.0001){       //when the difference b/w two vlaues is less than 0.0001
            break;
        }
        xm=xn;
        i++;
    }
    printf("root of the equation is %.4f",xn);
    return 0;
}






Output:













Name: Shubham Gosai
Course: Bsc IT 4B
University rollno: 2023102

Problem statement: Find root of the equation x^3=17 using secant method.

Formula:
Xn+1=xn-(f(xn)*(xn-xn-1))/(f(xn)-f(xn-1));

Source code:
#include<stdio.h>
#include<math.h>
float fuction(float x){
    return(pow(x,3)-17);        //given equation
}
int main(){
    int i=0;
    float x0=0.0,x1=1.0,x2;
    if(fuction(x0)==0){
printf("root of the equation is %.4f",x0);
        return 0;
}else if(fuction(x1)==0){
printf("root of the equation is %.4f",x1);
        return 0;
    }
    while((fuction(x0)*fuction(x1))>=0){        //condition to find range
        x0++;
        x1++;
    }
printf("range of the equation is from %.4f to %.4f\n",x0,x1);
printf("\nitr\tx0\tx1\tx2\tf(x2)\n\n");
i++;
    x2=x1-(fuction(x1)*(x1-x0))/(fuction(x1)-fuction(x0));      //formula used to find root
printf("%d\t%.4f\t%.4f\t%.4f\t%.4f\n",i,x0,x1,x2,fuction(x2));
    if(fuction(x2)>0){
        x1=x2;      //if f(x2) is +ve
}else if(fuction(x2)<0){
        x0=x2;      //if f(x2) is -ve
    }
while(1){
i++;
        x2=x1-(fuction(x1)*(x1-x0))/(fuction(x1)-fuction(x0));      //formula used to find root
        if((float)fabs(x2-x1)<=0.0001){     //condition to find root
            break;
        }
printf("%d\t%.4f\t%.4f\t%.4f\t%.4f\n",i,x0,x1,x2,fuction(x2));
        if(fuction(x2)>0){
            x1=x2;      //if f(x2) is +ve
}else if(fuction(x2)<0){
            x0=x2;      //if f(x2) is -ve
        }
    }
printf("root of the equation is %.4f",x2);
    return 0;
}
























Output:
