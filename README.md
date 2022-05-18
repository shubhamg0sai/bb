PROBLEM STATEMENT - Write a java program to create a class electricity and calculate the bill based on the following conditions
If unit < 100 bill=1.20* unit
Unit< 200 bill=(100*1.20)+(unit -100 *2)
Unit < 300 bill=(100*1.20)+(unit -100 *2)+(unit-200+3)

OBJECTIVE -To understand the concept of java ( object oriented language) .

EXPLAINATION – In java classes are categories and objects are items within each category . */

CODE-
import java.util.*;
class ElectricityBill
{
    public static void main(String args[])
    {
    Scanner sc = new Scanner(System.in);
int unit = 0;
        double bill=0.0;
System.out.println("Enter Unit: ");
        unit = sc.nextInt();
        if (unit<100)
        {
            bill=1.20*unit;
        }
        else if (unit<200)
        {
            bill =(100*1.20)+(unit-100*2);
        }
        else if (unit<300)
        {
            bill = (100*1.20)+(unit-100*2)+(unit - 200+3);
        }
        else
        {
System.out.println("invalid unit");
        }
System.out.println("Electricity bill is " +bill);
        }
    }
