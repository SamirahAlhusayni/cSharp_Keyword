# `break` keyword in C#
<div dir = "rtl"> 
أحد أوامر الانتقال أثناء تنفيذ البرنامج من نقطة الى أخرى، يستخدم هذا الامر للخروج من مجموعة الاوامر المغلقة بقوسين سواء switch أو loop ثم يمرر مؤشر التنفيذ الى النقطة التالية وهي التي تكون خارج هذه المجموعة  



الصيغة:
</div>

 `break`;
<div dir = "rtl"> 
 مثال:
 في هذا المثال  يتم المرور على الارقام من 1 - 100 ليتم طباعتها داخل أقواس loop ولكن بشرط أنه عندما يصبح الرقم يساوي القيمة 5 يتم إنهاء أمر الطباعة ويتم الخروج من هذه السطور البرمجية والتي هنا هي سطور for loop وانتقال مؤشر التنفيذ الى النقطة التالية مباشرة لذلك ستكون الطباعة حتى رقم 4 فقط 
</div>

    class BreakTest
    {
    static void Main()
    {
        for (int i = 1; i <= 100; i++)
        {
            if (i == 5)
            {
                break;
            }
            Console.WriteLine(i);
        }

        
        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
    }