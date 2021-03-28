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
               
                
                Console.WriteLine("Please enter your target?"); //Mis kirjutab konsoolis
                int UserTarget = int.Parse(Console.ReadLine());  //Loeb ja kirjutas konsoolis

                int Start = 0;  //algmuutuja on 0

                while (Start <= UserTarget)  //arv peab olema suurem kui 0 või varane
                {
                    Console.WriteLine(Start + " ");  //konsool võtab kokku
                    Start = Start + 2;  //lihtsalt tähendab start
                }

                do
                {
                    Console.WriteLine("Do you want continue - Yes or No ?");  // konsool küsib kaks vastuse variandid Yes või No?

                    UserChoice = Console.ReadLine().ToUpper();
                    if (UserChoice != "YES" && UserChoice != "NO") // konsool võtab ainult YES või NO
                    {
                        Console.WriteLine("Invalid Choice, please say Yes or No");  // kui kirjutab mitte Yes või No, siis küsib Yes või No
                    }
                } while (UserChoice != "Yes" && UserChoice != "No");  //Jah-ja ei-küsimuse väide while võrdsustab "JAH" asemel "JAH"
            } while (UserChoice == "YES"); //while võrdsustab "JAH" asemel "JAH"

        }
    }
    

Part 15 - C# Tutorial - for and foreach loops in c#.avi

    using System;
    class Program
    {
    static void Main()
    {
         int[] Numbers = new int[4];

          Numbers[0] = 101;  // number konsoolis
          Numbers[1] = 102;  // number konsoolis
          Numbers[2] = 103;  //number konsoolis
          Numbers[3] = 104;  //number konsoolis

        foreach (int k in Numbers)  //iga numbri jaoks number
        {
            Console.WriteLine(k);  //konsooli ütles see numbri
        }

          //for (int j = 0; j <= Numbers.Length; j++)  //esimene tingimuslik muutuja on 0, teine muutuja tsükli korduvate sammude arvu kontrollimiseks ja viimane osast i ++. See on iteratsioonilause - see käivitatakse pärast iga läbimist
        //{
          //  Console.WriteLine(Numbers[j]);  //konsool ütles number j
        //}

          //int i = 0;  //tingimuslik muutuja varane 0
          //while (i < Numbers.Length)  //tsüklis korduvate sammude arv on suurem kui muutuja
          //{
            //Console.WriteLine(Numbers[i]); //konsool ütleb muutuja
            //i++;  //liitmine
          //}
    }
    }
    
    
    using System;
    class Program
    {
    static void Main()
    {
         for (int i = 0; i <= 20; i++)  //esimene tingimuslik muutuja on 0, teine muutuja rohkem kui 20 või varane ja viimane osast i ++. See on iteratsioonilause - see käivitatakse pärast iga läbimist
        {
            if (i % 2 == 1)
                continue; //jätkata

            Console.WriteLine(i);  //konsool küsib muutujat
        }
    }
    }
    
Part 16 - C# Tutorial - Methods in c#.avi'

    using System;
    class Program
    {
    public static void Main()
    {
        Program.EvenNumbers(30);  //programmi number 30

        Program P = new Program();  // teeme uus programm
        int Sum = P.Add(10, 20);  //programmi summa

        Console.WriteLine("Sum = {0}", Sum);  //programm algab 0-st
    }

    public int Add(int  FN, int SN)
    {
        return FN + SN;  //tagastusväärtus
    }

    public static void EvenNumbers(int Target)  //on staatiline liige
    {
        int Start = 0;  //algmuutuja on 0

        while (Start <= Target)  //arv peab olema suurem kui 0 või varane
        {
            Console.WriteLine(Start);  //konsool ütleb start
            Start = Start + 2;  //lihtsalt tähendab start
        }
    }
    }
    
Part 17 - C# Tutorial - Method parameters.avi

    using System;
    class Program
    {
    public static void Main()
    {
        int i = 0;  //muutuja on 0

        SimpleMethod(ref i);  //muutuva läbimise meetod

        Console.WriteLine(i);  //konsool näitab muutuja
    }

    public static void SimpleMethod(ref int j)  //muutuva läbimise meetod
    {
        j = 101;  //muutuja
    }
    }
    
    
    using System;
    class Program
    {
    public static void Main()
    {
        int Total = 0;  //kokku 0
        int Product = 0;  //toote 0
        Calculate(10, 20, out Total, out Product);  //arvutama kokku ja toote

        Console.WriteLine("Sum = {0} && Product = {1}", Total, Product);  //konsool ütleb 
    }

    public static void Calculate(int FN, int SN, out int Sum, out int Product)
    {
        Sum = FN + SN;
        Product = FN + SN;
    }
   
    }
    
    
    using System;
    class Program
    {
    public static void Main()
    {
        int[] Numbers = new int[3];
        Numbers[0] = 101;
        Numbers[1] = 102;
        Numbers[2] = 103;

        //ParamsMethod();
        //ParamsMethod(Numbers);
        ParamsMethod(1, 2, 3, 4, 5);
    }

    public static void ParamsMethod(params int[] Numbers)
    {
        Console.WriteLine("There are {0} elemnts", Numbers.Length);

        foreach (int i in Numbers)  //muutuja numbris
        {
            Console.WriteLine(i);  //konsool ütleb muutuja
        }
    }

    }
    
 Konsool3 töö hulka
 
    using System;
    namespace RefVsOut
    {
    class Program
    {
        static void Main(string[] args)
        {
            int first = 1;  //esimene muutuja 1
            int second = 2;  //teine muutuja 2

            Method1(out first, out second);  //esimene meetod
            Method2(first, ref second);  //teine meetod
            Method3(ref first, second);  //kolmas meetod

            Console.WriteLine($"first: {first}, second: {second}");  // konsool küsib esimene ja teine numbrid
            Console.ReadLine();  //konsool ütles

        }

        static void Method1(out int a, out int b)
        {
            a = 2;  //tuntud muutuja
            b = 1;  //tuntud muutuja
        }

        static void Method2(int a, ref int b)
        {
            a *= 5;  //tuntud muutuja
            b *= a;  //tundmatu muutuja
        }

        static void Method3(ref int a, int b)
        {
            a *= 5;  //tuntud muutuja
            b *= b;  //tundmatu muutuja
        }
    }
    }


    
    














   
