# `object ` keyword in C#
<div dir = "rtl"> 
أحد Reference Types ، والذي يعتبر اسم مستعار عن System.Object والذي يمكن المستخدم أو المبرمج من تسجيل قيم من أي نوع من البيانات كما أ  قيمته الافتراضية هي null وعندما يكو النوع object  فإنها تشير الى عملة  boxing لانها تشير الى امكانية تجميع أكثر  من نوع في نوع واحد والعكس يسمى  unboxing




الصيغة:
</div>

    object obj;
    obj = 100; // this is boxing
<div dir = "rtl"> 
 مثال:
في هذا المثال تم استقبال متغير من نوع  object والتي تمكن الدالة من استقبال أي نوع بيانات لهذا المتغير
</div>
<div dir = "ltr"> 

        using System;

    namespace object
    {
    class Program
    {
        static void Main(string[] args)
        {   
            useparams2(1, 'a' , "test");
            public static void useparams2(params object[] list)
        {
            for (int i = 0; i < list.Length; i++)
            {
                Console.Write(list[i] + " ");
            }

            Console.WriteLine();
        }
    }
    }