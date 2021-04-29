# `params ` keyword in C#
<div dir = "rtl"> 
أحد Method Parameters ،عادة الـ method  عندما تستقبل  مصفوفة أحادية الأبعاد يكون محدد كم عدد عناصر المصفوفة بالاضافة الى أنها تكون مصفوفة من نوع واحد من البيانات لكن مع params يمكن أن ترسل مصفوفة من أنواع مختلفة من البيانات عندما تحدد نوع المصفوفة object أو أن ترسل مصفوفة من نوع واحد ولكن عدد عناصر غير محدد.

تشترط هذه الكلمة المفتاحية تحديد النوع المرسل قبل أقواس المصفوفة 

ملاحظة:
- عند وجود أكثر من متغير مرسل الى الـ method يتم وضع كلمة params قبل آخر متغير في رأس تعريف الدالة 

الصيغة:
</div>

    public static void functionName (params dataType[] arrayName)
    
    {
     
    }
<div dir = "rtl"> 
 مثال:
في هذا المثال تم تعريف دالتين الأولى إما أن يتم إرسال مصفوفة بشكل كامل أو يتم ارسال عدة عناصر من نوع واحد ولكن عددها غير معروف فتستقبلها الدالة التي تم تعريف المتغير فيها مسبوقا بكلمة params والدالة الثانية تم تعريف المتغير object والتي ستستقبل أي نوع من البيانات من غير تحديد عدد معين.
</div>
<div dir = "ltr"> 

        using System;

    namespace keyWordsParams
    {
    class Program
    {
        static void Main(string[] args)
        {      
           

           useparams(1, 2, 3, 4, 5, 6, 7);
            useparams2(1, 'a' , "test");

            int[] myIntArray = { 1, 2, 3, 4, 5, 6 };
            useparams(myIntArray);
            
        }
        public static void useparams (params int[] list )
        {
            for (int i = 0; i < list.Length; i++)
            {
                Console.Write(list[i] + " ");
            }

            Console.WriteLine();
        }

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
</div>