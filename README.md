# Test-Numbers
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Test_Numbers
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = int.Parse(Console.ReadLine());
            int b = int.Parse(Console.ReadLine());
            int maxNum = int.Parse(Console.ReadLine());

            int sum = 0;
            int count = 0;

            for (int i = a; i >= 1; i--)
            {
                for (int j = 1; j <= b; j++)
                {
                    sum += ((i * j) * 3);
                    
                    count++;

                    if (sum >= maxNum)
                    {
                        break;
                    }                    
                }
                if (sum >= maxNum)
                {
                    break;
                }
            }

            if (sum >= maxNum)
            {
                Console.WriteLine($"{count} combinations");
                Console.WriteLine($"Sum: {sum} >= {maxNum}");
            }
            else
            {
                Console.WriteLine($"{count} combinations");
                Console.WriteLine($"Sum: {sum}");
            }
        }
    }
}
