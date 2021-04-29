# `enum ` keyword in C#
<div dir = "rtl"> 
أحد Value Types ،والتي تعبر عن مجموعة من الثوابت مع بعضها والتي عادة ترتبط بقيم من نوع int تبدأ من صفر وتزيد بواحد مع كل عنصر جديد يتم إضافته، كما يمكن تغيير هذه القيم المرتبطة مع كل عنصر.



ملاحظة:
-  لايمكن تعريف method  داخل enum   وفي حال الرغبة في ذلك يتم عن طريق عملية extension method
-  يمكن استخدام هذا النوع لتمثيل مجوعة من الاختيارات عند تحديد enum  أنه سيكون [Flags]

الصيغة:
</div>

    enum CollectionName
    {
    item1,
    item2,
    ....,
    itwmn
    }
<div dir = "rtl"> 
 مثال:
في هذا المثال تم تعريف أيام الأسبوع والي تمثل مجموعة ثابتة من الأسماء، وتم تعريف مجموعة من الخيارات بالاعتماد على [Flags]
</div>
<div dir = "ltr"> 

        using System;

        namespace enumKeyWord
    {
    class Program
    {
        public enum Day { Sunday , Monday, Tueasday , Wednesday ,
                Thuresday, Friday, Saterday}

        [Flags]
        public enum BorderSide : byte { Left = 1, Right = 2, Top = 10, Bottom = 11 }
             
        static void Main(string[] args)
        {
            int weeStart = (int)Day.Sunday;
            Console.WriteLine(weeStart); // will print deafult value start with zero

            int Tueasdayinweek = (int)Day.Tueasday;
            Console.WriteLine(Tueasdayinweek); // will print the assigned value
            Day sun = (Day)weeStart;
            Console.WriteLine("the day is " + sun);


            Day fourth=(Day)3; // print element with associate value
            Console.WriteLine(fourth);



            // Challenge
           int borLeft = (int)BorderSide.Left; 
             BorderSide side = (BorderSide)borLeft;
             bool leftOrRigt = (int)side <= 2;

             Console.WriteLine($"Borderside from left  is {borLeft}");
             Console.WriteLine($"Borderside direction is {side}");
             BorderSide leftRight = BorderSide.Left | BorderSide.Right;
             Console.WriteLine("It's a left? " + leftOrRigt);

             string formatted = leftRight.ToString();
             Console.WriteLine(formatted);

		}
	}

    }

</div>