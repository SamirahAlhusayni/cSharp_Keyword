# `goto` keyword in C#

#### This keyword represent one of the jump statemets, it is used to transfers the program control directly to a labeled statement.

## Note:
 - Useful to get out of deeply nested loops.
 - Useful to transfer control to a specific switch-case label or the default label in a switch statement.


  

## `goto` syntax is : <br>
        goto labeled_statement;
        
  

## warning!
You must use condition to terminate this process before transfer the code into infinite loop.

## Example:

       using System;
    
    namespace program
    {
        class Program
        {
            static void Main(string[] args)
            {
                for (int i = 1; i < 10; i++)
                {
                    if (i == 5)
                    {
                        goto endloop;
                    }
                    Console.WriteLine("i value: {0}", i);
                }
            endloop: 
                Console.WriteLine("The end");
               
            }
        }
    }
