# mauuuuu





using System;

class Program
{
    static int GCD(int n1, int n2)
    {
        if (n1 == 0)
            return n2;
        if (n2 == 0)
            return n1;
        if (n1 == n2)
            return n1;

        if (n1 < n2)
            return GCD(n1, n2 % n1);
        else
            return GCD(n1 % n2, n2);
    }

    static void Main(string[] args)
    {
        int num1 = 124;
        int num2 = 31;
        int gcd = GCD(num1, num2);

        Console.WriteLine("GCD of the numbers {0} {1} are: {2}", num1, num2, gcd);
    }
}
