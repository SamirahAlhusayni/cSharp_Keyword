# `class` keyword in C#

#### In c#, Class is a data structure, and it will combine various types of data members such as fields, properties, member functions, and events into a single unit. 


## `class` declaration  syntax is :
 <br>

        public class users {

        // Properties, Methods, Events, etc.

        }
        
  
  ## Note:
 - Here, the public access specifier will allow the users to create objects for this class, and inside of the body class, we can create required fields, properties, methods, and events to use in our applications.

## warning!
 You can used various data members like access modifiers, fields, properties, methods, constructors, etc., in your c# class based on your requirements. 

## Example:

    public class Users
    {
     public int id = 0;
     public string name = string.Empty;
     public Users()
     {
        // Constructor Statements
     }
     public void GetUserDetails(int uid, string uname)
     {
         id = uid;
         uname = name;
         Console.WriteLine("Id: {0}, Name: {1}", id, name);
     }
     public int Designation { get; set; }
     public string Location { get; set; }
    }

    
