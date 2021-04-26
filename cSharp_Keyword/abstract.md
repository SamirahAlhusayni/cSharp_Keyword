# `abstract` keyword in C#

#### This keyword represent one of the access modifires in c#, and it is useful to define classes and class members that are needed to be implemented or overridden in a derived class.
## Note:
 - You can use with classes, methods, properties, indexers, and events.
 - The members we defined as abstract or included in an abstract class must be implemented by classes derived from an abstract class.
 -   If we define a class with abstract modifier, then that class is intended only to be used as a base class for other classes.
 -  The abstract class cannot instantiate, and it can contain both abstract and non-abstract members.
  


        
  


## warning!
In c#, we should not use a sealed keyword with an abstract class because the sealed keyword will make a class not inheritable but abstract modifier requires a class to be inherited. 

## Example:
### example of defining an abstract class using abstract keyword.

    using System;

    namespace Tutlane
    {
    abstract class Info
    {
       abstract public void GetDetails(string x, string y, int z);
    }
    class User: Info
    {
       public override void GetDetails(string a, string b, int c)
       {
           Console.WriteLine("Name: {0}", a);
           Console.WriteLine("Location: {0}", b);
           Console.WriteLine("Age: {0}", b);
       }
    }
    class Program
    {
       static void Main(string[] args)
       {
           User u = new User();
           Console.WriteLine("****Abstract Class Example****");
           u.GetDetails("Suresh Dasari", "Hyderabad", 32);
           Console.ReadLine();
       }
    }
    }