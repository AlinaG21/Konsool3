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
    
    
    using System;
    class Program
    {
    static void Main()
    {
         for (int i = 0; i <= 20; i++)
        {
            if (i % 2 == 1)
                continue;

            Console.WriteLine(i);
        }
    }
    }
    
Part 16 - C# Tutorial - Methods in c#.avi'

    using System;
    class Program
    {
    public static void Main()
    {
        Program.EvenNumbers(30);

        Program P = new Program();
        int Sum = P.Add(10, 20);

        Console.WriteLine("Sum = {0}", Sum);
    }

    public int Add(int  FN, int SN)
    {
        return FN + SN;
    }

    public static void EvenNumbers(int Target)
    {
        int Start = 0;

        while (Start <= Target)
        {
            Console.WriteLine(Start);
            Start = Start + 2;
        }
    }
    }
    
Part 17 - C# Tutorial - Method parameters.avi

    using System;
    class Program
    {
    public static void Main()
    {
        int i = 0;

        SimpleMethod(ref i);

        Console.WriteLine(i);
    }

    public static void SimpleMethod(ref int j)
    {
        j = 101;
    }
    }












   
