# `as` keyword in C#

#### This keyword represent one of the conversion type operators, it is used to  explicitly convert an expression to a given type if <b> its runtime type is compatible with that type</b> 
## Note:
 - Convert to reference or nullable values
 - If the conversion is not possible, the `as` operator returns null. <b> Unlike a cast expression, the as operator never throws an exception.</b>
 -  Actually, the `as operator fulfills a similar role like "is" but in a slightly truncated manner
 -  The is operator is of boolean type whereas as operator is not of boolean type.
 -  The is operator returns false if the given object is not of the same type whereas as operator return null if the conversion is not possible.

## `AS` syntax is : <br>
        E as T
        
  
  - E is  is an expression that returns a value.
  - T is the name of a type or a type parameter.

## warning!
You cannot use the as operator to perform a user-defined conversion. 

## Example:

    using System;
    class child
    {
    public void Speak() { Console.WriteLine("Play!"); }
    }
    class Example
    {
    static void Main()
    {
    Object obj = new child();
    child son = obj as child;
    if (son != null)
    son.Speak();
    }
    
    }
