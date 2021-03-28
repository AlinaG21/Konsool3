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
    

Part 15 - C# Tutorial - for and foreach loops in c#.avi

    using System;
    class Program
    {
    static void Main()
    {
         int[] Numbers = new int[4];

          Numbers[0] = 101;
          Numbers[1] = 102;
          Numbers[2] = 103;
          Numbers[3] = 104;

        foreach (int k in Numbers)
        {
            Console.WriteLine(k);
        }

          //for (int j = 0; j <= Numbers.Length; j++)
        //{
          //  Console.WriteLine(Numbers[j]);
        //}

          //int i = 0;
          //while (i < Numbers.Length)
          //{
            //Console.WriteLine(Numbers[i]);
            //i++;
          //}
    }
    }





   
