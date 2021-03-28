# Konsool3
using System;

namespace ConsoleApp5
{
    class Program
    {
        static void Main()
        {
            Console.WriteLine("Please enter your target?");
            int UserTarget = int.Parse(Console.ReadLine());

            int Start = 0;

            while(Start <= UserTarget)
            {
                Console.WriteLine(Start + " ");
                Start = Start + 2;
            }
        }
    }
}
