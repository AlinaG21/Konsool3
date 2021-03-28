# Konsool3

Part 14 - C# Tutorial - do while loop in c#

using System;

    class Program
    {
        static void Main()
        {
            string UserChoice = string.Empty;
            do
            {

                Console.WriteLine("Please enter your target?");
                int UserTarget = int.Parse(Console.ReadLine());

                int Start = 0;

                while (Start <= UserTarget)
                {
                    Console.WriteLine(Start + " ");
                    Start = Start + 2;
                }

                do
                {
                    Console.WriteLine("Do you want continue - Yes or No ?");

                    UserChoice = Console.ReadLine().ToUpper();
                    if (UserChoice != "YES" && UserChoice != "NO")
                    {
                        Console.WriteLine("Invalid Choice, please say Yes or No");
                    }
                } while (UserChoice != "Yes" && UserChoice != "No");
            } while (UserChoice == "YES");

        }
    }



   
