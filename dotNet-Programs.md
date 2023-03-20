## Program that prints "Hello World" to the console:

    using System;

    namespace HelloWorld
    {
        class Program
        {
            static void Main(string[] args)
            {
                Console.WriteLine("Hello World!");
                Console.ReadLine();
            }
        }
    }

This program uses the Console.WriteLine method to print the string "Hello World" to the console. The Console.ReadLine method is included to prevent the console window from closing immediately after the program is executed.

<hr>

## program that generates the Fibonacci series:

    using System;

    namespace Fibonacci
    {
        class Program
        {
            static void Main(string[] args)
            {
                int n1 = 0, n2 = 1, n3, i, number;
                Console.Write("Enter the number of elements: ");
                number = int.Parse(Console.ReadLine());
                Console.Write(n1 + " " + n2 + " "); // printing 0 and 1
                for (i = 2; i < number; ++i) // loop starts from 2 as 0 and 1 are already printed
                {
                    n3 = n1 + n2;
                    Console.Write(n3 + " ");
                    n1 = n2;
                    n2 = n3;
                }
            }
        }
    }

This program prompts the user to enter the number of elements to generate in the Fibonacci series. It then uses a loop to generate and print the series up to the specified number of elements. The program uses three integer variables n1, n2, and n3 to keep track of the current, next, and sum of the previous two elements in the series, respectively. The Console.ReadLine method is included to prevent the console window from closing immediately after the program is executed.

<hr>

## Program to check whether a given string is a palindrome or not:

    using System;

    class PalindromeChecker {
        static void Main() {
            Console.Write("Enter a string: ");
            string str = Console.ReadLine();

            // Remove spaces and convert to lowercase
            str = str.Replace(" ", "").ToLower();

            // Check if the string is a palindrome
            bool isPalindrome = true;
            int length = str.Length;
            for (int i = 0; i < length / 2; i++) {
                if (str[i] != str[length - i - 1]) {
                    isPalindrome = false;
                    break;
                }
            }

            if (isPalindrome) {
                Console.WriteLine("{0} is a palindrome.", str);
            } else {
                Console.WriteLine("{0} is not a palindrome.", str);
            }
        }
    }

In this program, we first prompt the user to enter a string. We then remove any spaces from the string and convert it to lowercase to make the palindrome check case-insensitive.

We then check if the string is a palindrome by comparing the first character with the last character, the second character with the second last character, and so on. If any of these pairs of characters are not equal, we know that the string is not a palindrome.

Finally, we output whether the string is a palindrome or not to the console.

<hr>

## Program that calculates the sum of numbers:

    using System;

    class Program
    {
        static void Main(string[] args)
        {
            int n, i, sum = 0;
            Console.WriteLine("Enter the value of n:");
            n = int.Parse(Console.ReadLine());
            for (i = 1; i <= n; i++)
            {
                sum += i;
            }
            Console.WriteLine("The sum of numbers from 1 to {0} is {1}", n, sum);
            Console.ReadLine();
        }
    }

This program prompts the user to enter a value for n, then calculates the sum of numbers from 1 to n using a for loop. Finally, it displays the result using the Console.WriteLine method.

<hr>

## Program to check if a given number is prime or not:

    using System;

    class PrimeNumberChecker {
        static void Main(string[] args) {
            int num;
            bool isPrime = true;

            Console.Write("Enter a number: ");
            num = Convert.ToInt32(Console.ReadLine());

            for (int i = 2; i <= num / 2; i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }

            if (isPrime) {
                Console.WriteLine(num + " is a prime number.");
            } else {
                Console.WriteLine(num + " is not a prime number.");
            }
        }
    }

The program takes an input number from the user and then checks whether it is divisible by any number between 2 and half of the given number. If it is divisible by any number, then the number is not prime, otherwise it is prime.

<hr>

## Binary Search Algorithm

    using System;

    class BinarySearchExample
    {
        static int BinarySearch(int[] arr, int x)
        {
            int left = 0, right = arr.Length - 1;
            while (left <= right)
            {
                int mid = left + (right - left) / 2;
                if (arr[mid] == x)
                    return mid;
                if (arr[mid] < x)
                    left = mid + 1;
                else
                    right = mid - 1;
            }
            return -1;
        }

        static void Main()
        {
            int[] arr = { 2, 3, 4, 10, 40 };
            int x = 10;
            int result = BinarySearch(arr, x);
            if (result == -1)
                Console.WriteLine("Element not found");
            else
                Console.WriteLine("Element found at index " + result);
        }
    }

In this example, the BinarySearch function takes an array of integers and the value to search for as input parameters. It then uses the binary search algorithm to locate the index of the given value in the array, or returns -1 if the value is not found.

The Main function initializes an array and a search value, and calls the BinarySearch function to find the index of the value in the array. It then prints the result to the console.

## Linear Search Algorithm

    using System;

    class Program
    {
        static int LinearSearch(int[] arr, int x)
        {
            int n = arr.Length;
            for (int i = 0; i < n; i++)
            {
                if (arr[i] == x)
                {
                    return i;
                }
            }
            return -1;
        }

        static void Main(string[] args)
        {
            int[] arr = { 2, 3, 4, 10, 40 };
            int x = 10;

            int result = LinearSearch(arr, x);
            if (result == -1)
            {
                Console.WriteLine("Element not found");
            }
            else
            {
                Console.WriteLine("Element found at index " + result);
            }
        }
    }
    
This program demonstrates a linear search algorithm to find an element x in an integer array arr. The LinearSearch function takes the array and the element to be searched as input parameters and returns the index of the element if found, otherwise returns -1. In the Main function, an integer array arr and an element x are defined, and the LinearSearch function is called to search for the element x in the array arr. If the element is found, the index of the element is printed, otherwise a message indicating that the element was not found is printed.

<hr>

## String Reversal Program

    using System;

    class stringReverse
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter a string: ");
            string str = Console.ReadLine();

            char[] charArray = str.ToCharArray();
            Array.Reverse(charArray);

            string reversedStr = new string(charArray);
            Console.WriteLine("Reversed string: " + reversedStr);
        }
    }

The program first prompts the user to enter a string. It then converts the string to a character array and uses the Array.Reverse() method to reverse the order of the elements in the array. Finally, it creates a new string from the reversed character array and outputs it to the console.
