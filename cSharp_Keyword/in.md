# `in` keyword in C#
<div dir = "rtl"> 
أحد  الـ parameter modifier والتي تساعد في تمرير Reference للمعامل وليس فقط قيمته ولكنها تضمن عدم التغيير على هذا الـ argument، وتختلف عن  out و  ref أنه لا حاجة  لكتابتها في الاستدعاء وانما فقط تكتب في تعريف وmethod 

الصيغة: لا تضاف الى جانب المعامل عند استدعائه وانما إلى جانب المتغير نفسه عند تعريف الـ method
</div>

 `in`;
 
<div dir = "rtl"> 
 مثال:
 في هذا المثال تم تعريف متغير i مع إسناد قيمة له ثم تمرير reference الى method  أخرى بشرط ضمان عدم حصول أي تغيرات على المتغير فسيتم الاحتفاظ بالقيمة 8 في هذا المثال.
</div>

    using System;
    public class Program
    {
   
    public static void upload(in int d)
    {
        _ = d * 2;
    }
    public static void Main()
    {
     
        int i = 8;
        Program p1 = new Program();
       
        upload(i);
        Console.WriteLine("Changed value is: {0}", i);
    }
    }   