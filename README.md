# Assignment-3
Prime numbers

using System;

namespace Prime_numbers
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("This program allows you to find all prime numbers till the number that you enter.");
            Console.WriteLine("Please enter a number.");
            int input = Convert.ToInt32(Console.ReadLine());
            bool nonprime = true;
            int n = 999999999;
            bool[] numbers = new bool[n];
            for (int i = 2; i < input; i++)
            {
                numbers[i] = true;
            }
            numbers[0] = false; numbers[1] = false;
            for (int i = 0; i < input; i++)
            {
                if (numbers[i])
                {
                    nonprime = false;
                    Console.WriteLine(i +" is a prime number");
                    for (int j = 2; (i) * j < input; j++ )
                    
                    {
                        numbers[(i) * j] = false;

                    }
                }
          }
            if(nonprime)
            {
                Console.WriteLine("There is no prime number till the number that you enter.");
            }
        }
        }
    }

