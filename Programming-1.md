# 100-coding-questions

### 1. Find a number is positive or negative ?

```java  
class Main
{
  public static void main (String[]args)
  {

    int num = 5;

    if (num > 0)
        System.out.println ("The number is positive");
    else if (num < 0)
        System.out.println ("The number is negative");
    else
        System.out.println ("Zero");
  }
}
```


### 2. Find a number is Even or Odd?

```java
// Using Modulus Operator
public class Main
 {
      public static void main(String[] args) {
           int number = 29;


     //checking whether the number is even or odd
     if (number % 2 == 0)
              System.out.println(number + " is Even");
     else
              System.out.println(number + " is odd");
      }
 }
```
```java
// Using Bitwise Operator
public class Main
{
  public static void main (String[]args)
  {
    int number = 29;

    if (isEven (number))
        System.out.println ("Even");
    else
        System.out.println ("Odd");
  }


// Returns true if n is even, else odd
  static bool isEven (int number)
  {

    // n & 1 is 1, then odd, else even
    return (!(number & 1));
  }
}
```
### 3. Find the Sum of First N Natural Numbers in Java

```java
//using loops
public class Main
 {
   public static void main (String[]args)
   {

     int n = 10;
     int sum = 0;

     for (int i = 1; i <= n; i++)
         sum += i;
       System.out.println (sum);
   }
 }
 ```
 ```java
 //using formula
 public class Main
 {
   public static void main (String[]args)
   {

     int n = 10;

       System.out.println ( n*(n+1)/2);
   }
 }
 ```

 ### 4. Find the Sum of the Numbers in a Given Interval in Java
 ```java
 
 //Using Brute Force
public class Main
{
  public static void main (String[]args)
  {
    int a = 5;
    int b = 10;

    int sum = 0;

    for (int i = a; i <= b; i++)
        sum = sum + i;
      System.out.println ("The sum is " + sum);
  }
}
```


```java

//using formula
public class Main
{
	public static void main(String[] args) {
	    int num1 = 2;
	    int num2 = 5;
	    int sum = num2*(num2+1)/2 - num1*(num1+1)/2 + num1;
		System.out.println("The Sum is "+ sum);
	}
}
```


### 5. Find the Greatest of the Three Numbers in Java

```java

//using conditional statements
public class Main
{
  public static void main (String[]args)
  {

    int num1 = 10, num2 = 20, num3 = 30;

    //checking if num1 is greatest
    if (num1 >= num2 && num1 >= num3)
        System.out.println (num1 + " is the greatest");

    //checking if num2 is greatest
    else if (num2 >= num1 && num2 >= num3)
        System.out.println (num2 + " is the greatest");

    //checking if num2 is greatest
    else if (num3 >= num1 && num3 >= num2)
        System.out.println (num3 + " is the greatest");
  }
}
```



```java

public class Main
{
  public static void main (String[]args)
  {

    int num1 = 10, num2 = 20, num3 = 30;

     int temp, result;    
    
    // find the largest b/w num1 and num2 & store in temp
    temp = num1>num2 ? num1:num2;
    
    // find the largest b/w temp and num3 & finally printing it
    result = temp>num3 ? temp:num3;  
    System.out.println (result + " is the greatest");
  }
}
```


### 6. Check Whether or Not the Year is a Leap Year in Java

```java
import java.util.Scanner;

public class LeapYear {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter the year :");
		int n = sc.nextInt();//
		boolean result = leapYear(n);
		System.out.println(result);
	}
	public static boolean leapYear(int n) {
		if(n%4 == 0)
		{
			if(n%100 == 0)
			{
				if(n%400 == 0)
				{
					return true;
				}
				else {
					return false;
				}
			}
			else {
				return true;
			}
		}
		else {
			return false;
		}
	}
}
```


### 7. Check if the given number is prime or not in Java

```java
import java.util.Scanner;

public class PrimeNumber {
	public static boolean isPrime(int num)
	{
		boolean flag = true;
		for(int i=2;i<= num/2;i++)
		{
			if(num%i == 0)
			{
				flag = false;
				break;
			}
		}
		
		return flag;
	}
	public static void main(String[] args) {
		//To collect input
		Scanner sc = new Scanner(System.in);
		System.out.println("Enter the number to be checked :");
		//the number to be checked is stored inside num
		int num = sc.nextInt();
		
		//calling isPrime(num) by passing num as the parameter
		boolean result = isPrime(num);
		if(result == true) 
		{
			System.out.println("Given Number is a Prime number");
		}
		else 
		{
			System.out.println("Given Number is not a Prime Number");
		}
	}
}
```					 


### 8. Find all the Prime Numbers in a Given Interval in Java

```java
public class Main
 {
   public static void main (String[]args)
   {

     int lower = 1, upper = 20;


     for (int i = lower; i <= upper; i++)
       if (isPrime (i))
        System.out.println (i);
   }

   static boolean isPrime (int n)
   {
     int count = 0;

     // 0, 1 negative numbers are not prime
     if (n < 2)
       return false;

     // checking the number of divisors b/w 1 and the number n-1
     for (int i = 2; i < n; i++)
       {
     if (n % i == 0)
        return false;
       }

     // if reached here then must be true
     return true;
   }
 }
```			   

 
 ### 9. Find the Sum of the Digits of a Number in Java Language

 ```java
 public class Main
 {
   public static void main (String[]args)
   {

     int num = 12345, sum = 0;
       System.out.println ("Sum of digits : " + getSum (num, sum));
   }

   static int getSum (int num, int sum)
   {

     if (num == 0)
       return sum;

     sum += num % 10;
     return getSum (num / 10, sum);
   }
 }
```

 
### 10. Find the Reverse of a Number in Java Language

```java
public class Main
{
    public static void main (String[]args)
    {

        //variables initialization
        int num = 1234, reverse = 0, rem;


        //loop to find reverse number
        while (num != 0)
        {
            rem = num % 10;
            reverse = reverse * 10 + rem;
            num /= 10;
        };

        //output
        System.out.println ("Reversed Number: " + reverse);
    }
}
```


### 11. Check Whether or Not the Number is a Palindrome in Java Language

```java
public class Main
 {
   public static void main (String[]args)
   {
     //variables initialization
     int num = 12021, reverse = 0, rem, temp;

       temp = num;
     //loop to find reverse number
     while (temp != 0)
       {
     	rem = temp % 10;
     	reverse = reverse * 10 + rem;
     	temp /= 10;
       };

     // palindrome if num and reverse are equal
     if (num == reverse)
       System.out.println (num + " is Palindrome");
     else
       System.out.println (num + " is not Palindrome");
   }
 }
```

 
 ### 12. Check Whether or Not the Number is an Armstrong Number

 ```java
 import java.util.*;
import java.lang.*;

class Main {

    // Driver code
    public static void main(String[] args)
    {
        //variables initialization
        int num = 1634, reverse = 0;
        int len = order(num);

        if (num == getArmstrongSum(num, len))
            System.out.println(num + " is an Armstrong Number");
        else
            System.out.println(num + " is not an Armstrong Number");

    }

    private static int getArmstrongSum(int num, int order) {
        if(num == 0)
            return 0;

        int digit = num % 10;

        return (int) Math.pow(digit, order) + getArmstrongSum(num/10, order);
    }

    private static int order(int num) {
        int len = 0;
        while (num!=0)
        {
            len++;
            num = num/10;
        }
        return len;
    }

}


### 13. Find the Armstrong Numbers in a given Range using Java


```java
import java.util.Scanner;

public class LearnCoding2
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter lower and upper ranges : ");
        int low = sc.nextInt();
        int high = sc.nextInt();

        System.out.println("Armstrong numbers between "+ low + " and " + high + " are : ");

        // loop for finding and printing all armstrong numbers between given range
        for(int num = low ; num <= high ; num++)
        {
            int len = getOrder(num);

            if(num == getArmstrongSum(num, len))
                System.out.print(num + " ");
        }

    }

    private static int getOrder(int num) {
            int len = 0;
            while (num!=0)
            {
                len++;
                num = num/10;
            }
            return len;
    }
    private static int getArmstrongSum(int num, int order) {
        if(num == 0)
            return 0;

        int digit = num % 10;

        return (int) Math.pow(digit, order) + getArmstrongSum(num/10, order);
    }
}
```


### 14. Find the Fibonacci Series up to Nth Term in Java Language

```java
public class Main
 {
   public static void main (String[]args)
   {

     int num = 15;
     int a = 0, b = 1;

     // Here we are printing 0th and 1st terms
       System.out.print (a + " , " + b + " , ");

     int nextTerm;

     // printing the rest of the terms here
     for (int i = 2; i < num; i++)
       {
      nextTerm = a + b;
      a = b;
          b = nextTerm;
          System.out.print (nextTerm + " , ");
       }


   }
 }
```


 ### 15. Factorial of a Number in Java

 ```java
 class Main
{
    // Method to find factorial of the given number
    static int factorial(int n)
    {
        int res = 1, i;
        for (i = 2; i <= n; i++)
            res *= i;
        return res;
    }
    
    // Driver method
    public static void main(String[] args)
    {
        int num = 6;
        System.out.println("Factorial of " + num + " is " + factorial(num));
    }
}
```



### 16. Program to check if the given 2 strings are anagrams.

1. Convert the string to a character array
2. sort the array
3. check the equality of the 2 arrays.


```java
import java.util.Arrays;

public class Anagram {
    public static boolean isAnagram(String str1, String str2) {
        // Remove all whitespace and convert to lowercase
        str1 = str1.replaceAll("\\s", "").toLowerCase();
        str2 = str2.replaceAll("\\s", "").toLowerCase();

        // Check if the two strings have the same length
        if (str1.length() != str2.length()) {
            return false;
        }

        // Convert both strings to char arrays and sort them
        char[] charArray1 = str1.toCharArray();
        char[] charArray2 = str2.toCharArray();
        Arrays.sort(charArray1);
        Arrays.sort(charArray2);

        // Compare the sorted char arrays
        return Arrays.equals(charArray1, charArray2);
    }

    public static void main(String[] args) {
        String str1 = "restful";
        String str2 = "fluster";
        if (isAnagram(str1, str2)) {
            System.out.println(str1 + " and " + str2 + " are anagrams.");
        } else {
            System.out.println(str1 + " and " + str2 + " are not anagrams.");
        }
    }
}
```



### 17. Write a program to count the number of words in the given string
1. check for spaces in the given string
2. count the spaces inside a third party variable
3. Add 1 to the total space count to find the total number of words.

```java
public class WordCounter {
    public static int countWords(String str) {
        int wordCount = 0;

        // Split the string into words using whitespace as the delimiter
        String[] words = str.split("\\s+");

        // Count the number of words
        wordCount = words.length;

        return wordCount;
    }

    public static void main(String[] args) {
        String str = "This is a test string.";
        int wordCount = countWords(str);
        System.out.println("The number of words in the string is: " + wordCount);
    }
}
```



### 18. Write a program to find the count of all the uppercase letters in the given string
1. Identify the ASCII value for A and Z (A=65 and Z=90)
2. use a conditional statement to check if the character being checked falls under the given ranges
3. if yes increment count

```java
public class UppercaseCounter {
    public static int countUppercase(String str) {
        int uppercaseCount = 0;

        // Iterate through each character in the string
        for (int i = 0; i < str.length(); i++) {
            char c = str.charAt(i);
            if (Character.isUpperCase(c)) {
                uppercaseCount++;
            }
        }

        return uppercaseCount;
    }

    public static void main(String[] args) {
        String str = "This is a Test String.";
        int uppercaseCount = countUppercase(str);
        System.out.println("The number of uppercase letters in the string is: " + uppercaseCount);
    }
}

```

### 19. Write a program to print the smallest and biggest numbers in an array.

```java
import java.util.Arrays;

public class MinMaxFinder {
    public static void main(String[] args) {
        int[] arr = {10, 5, 7, 25, 30, 2};
        
        // Sort the array in ascending order
        Arrays.sort(arr);
        
        // Print the smallest and largest elements of the array
        System.out.println("Smallest element: " + arr[0]);
        System.out.println("Largest element: " + arr[arr.length - 1]);
    }
}

```

### 20. Find the Factorial of the given Number in Java
1. Call function getFactorial(num)
2. Set base case when num == 0 return 1
3. Other cases return num * getFactorial(num-1);

```java
import java.util.Scanner;

public class FactorialFinder {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        
        int factorial = 1;
        
        // Calculate the factorial of n
        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }
        
        System.out.println("Factorial of " + n + " is " + factorial);
    }
}

```

### 21. Check Whether or Not the given Number is an Armstrong Number

370 = 3^3 + 7^3 + 0^3 = 27 + 343 + 0 = 370

```java
import java.util.Scanner;

public class ArmstrongChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();

        int num = n;
        int sum = 0;
        int digits = String.valueOf(n).length();
        
        // Calculate the sum of the cubes of the digits
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        // Check if the number is an Armstrong number
        if (sum == n) {
            System.out.println(n + " is an Armstrong number.");
        } else {
            System.out.println(n + " is not an Armstrong number.");
        }
    }
}

```

### 22. Check if the given number is a Perfect Square using Java

```Java
import java.util.Scanner;

public class PerfectSquareChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        
        boolean isPerfectSquare = false;
        
        // Check if the number is a perfect square
        for (int i = 1; i <= n; i++) {
            if (i * i == n) {
                isPerfectSquare = true;
                break;
            }
        }
        
        if (isPerfectSquare) {
            System.out.println(n + " is a perfect square.");
        } else {
            System.out.println(n + " is not a perfect square.");
        }
    }
}

```

### 23. Program for Finding out the Prime Factors of a number in Java

```java
import java.util.Scanner;

public class PerfectSquareChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        
        boolean isPerfectSquare = false;
        
        // Check if the number is a perfect square
        for (int i = 1; i <= n; i++) {
            if (i * i == n) {
                isPerfectSquare = true;
                break;
            }
        }
        
        if (isPerfectSquare) {
            System.out.println(n + " is a perfect square.");
        } else {
            System.out.println(n + " is not a perfect square.");
        }
    }
}

```

### 24. Program to find the power of a number using Java

```java
import java.util.Scanner;

public class PrimeFactorFinder {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = scanner.nextInt();
        
        System.out.print("Prime factors of " + n + ": ");
        
        // Find the prime factors of n
        for (int i = 2; i <= n; i++) {
            while (n % i == 0) {
                System.out.print(i + " ");
                n /= i;
            }
        }
        
        System.out.println();
    }
}

```


### 25. Program to find factors of a number using Java

```java
import java.util.Scanner;

public class FactorFinder {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int num = input.nextInt();
        
        System.out.print("Factors of " + num + " are: ");
        for (int i = 1; i <= num; i++) {
            if (num % i == 0) {
                System.out.print(i + " ");
            }
        }
    }
}

```

### 26. Check Whether or Not the Given Number is a Strong Number in Java Language

```java
import java.util.Scanner;

public class StrongNumberChecker {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int num = input.nextInt();
        
        int originalNum = num;
        int sum = 0;
        while (num > 0) {
            int digit = num % 10;
            int factorial = 1;
            for (int i = digit; i > 0; i--) {
                factorial *= i;
            }
            sum += factorial;
            num /= 10;
        }
        
        if (sum == originalNum) {
            System.out.println(originalNum + " is a strong number.");
        } else {
            System.out.println(originalNum + " is not a strong number.");
        }
    }
}

```
### 27. Program to check if the given number is an Automorphic number or not using Java

```java
import java.util.Scanner;

public class AutomorphicNumberChecker {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a positive integer: ");
        int num = input.nextInt();
        
        int square = num * num;
        int count = 0;
        int originalNum = num;
        
        while (num > 0) {
            count++;
            num /= 10;
        }
        
        int lastDigits = (int) (square % (Math.pow(10, count)));
        
        if (lastDigits == originalNum) {
            System.out.println(originalNum + " is an Automorphic number.");
        } else {
            System.out.println(originalNum + " is not an Automorphic number.");
        }
    }
}

```

### 28. Binary to decimal conversion using Java


```java

import java.util.Scanner;
public class Main
{
	public static void main(String args[])
	{
		Scanner sc = new Scanner(System.in);    
		System.out.print("Enter a binary number : ");
		int binary = sc.nextInt();
		//Declaring variable to store decimal number  
		int decimal = 0;
		//Declaring variable to use in power		
		int n = 0;  
		//writing logic for the conversion
		while(binary > 0)
		{
			int temp = binary%10; 
			decimal += temp*Math.pow(2, n);  
			binary = binary/10;  
			n++;  
		}
		System.out.println("Decimal number : "+decimal); 
                //closing scanner class(not compulsory, but good practice)
		sc.close();
	}
}
```



### 29. Octal to decimal conversion in Java

```java
import java.util.Scanner;
public class Main
{
	public static void main(String args[])
	{      
		//scanner class object creation
		Scanner sc = new Scanner(System.in);    
		//input from user
		System.out.print("Enter a octal number : ");
		int octal = sc.nextInt();
		//Declare variable to store decimal number  
		int decimal = 0;
		//Declare variable to use in power		
		int n = 0;  
		//writing logic for the conversion
		while(octal > 0)
		{
			int temp = octal % 10;  
			decimal += temp * Math.pow(8, n);  
			octal = octal/10;  
			n++;  
		}
		//printing result
		System.out.println("Decimal number : "+decimal); 
		//closing scanner class(not compulsory, but good practice)
		sc.close();   
	}
}

```

