import java.util.Scanner;
public class FibonacciCLA 
{
    public static void main(String[] args) 
    {
        int n, a = 0, b = 0, c = 1;
        Scanner s = new Scanner(System.in);
        System.out.print("Enter value of n:");
        n = s.nextInt();
        System.out.print("Fibonacci Series:");
        for(int i = 1; i <= n; i++)
        {
            a = b;
            b = c;
            c = a + b;
            System.out.print(a);
        }
    }
}

/*

class FibonacciCLA
{
public static void main(String args[])
{
int a=0,b=1,c=0;
int n=Integer.parseInt(args[0]);
for(int i=1;i<n-1;i++)
{
System.out.print(a);
c=a+b;
a=b;
b=c;
}
}
}
*/
