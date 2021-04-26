# `delegate` keyword in C#

#### In c#, the delegate is a type that defines a method signature, and it is useful to hold the reference of one or more methods which are having the same signatures. 

## `delegate` syntax is : <br>
     <access_modifier> delegate <return_type> <delegate_name>()
        


## Example:

    using System;

    namespace Tutlane
    {
    // Declare Delegate
    public delegate void SampleDelegate(int a, int b);
    class MathOperations
    {
        public void Add(int a, int b)
        {
            Console.WriteLine("Add Result: {0}", a + b);
        }
        public void Subtract(int x, int y)
        {
            Console.WriteLine("Subtract Result: {0}", x - y);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("****Delegate Example****");
            MathOperations m = new MathOperations();
            // Instantiate delegate with add method
            SampleDelegate dlgt = m.Add;
            dlgt(10, 90);
            // Instantiate delegate with subtract method
            dlgt = m.Subtract;
            dlgt(10, 90);
            Console.WriteLine();
        }
    }
    }