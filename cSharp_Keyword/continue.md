# `continue` keyword in C#
<div dir = "rtl"> 
أحد أوامر الانتقال أثناء تنفيذ البرنامج من نقطة الى أخرى، نستخدم هذا الامر لنقل البرنامج للخطوة التالية من المرحلة في loop سواء while / do / for. نستيطع أن نعتبره اختبار شرط اذا وصل له البرنامج فهذا يعني تجاوز السطور البرمجية الموجودة في الجولة الحالية وانتقل للجولة التالية.
 



الصيغة:
</div>

 `continue`;
<div dir = "rtl"> 
 مثال:
 في هذا المثال تم تعريف متغير واسناد قيمة 10 له، وتم تنفيذ عملية الزيادة عليه بواحد ولكن بشرط في جال أصبحت قيمته 15 يتم تجاوزها ولا تؤخذ ثم يتم الانتقال للمرحلة التالية بغض النظر عن وجود الأسطر البرمجية لذلك لن يتم طباعة الرقم 15 وانما تم تجاوزه
</div>

    namespace Loops
    {
    class Program
    {
        static void Main(string[] args)
        {
            /* local variable definition */
            int a = 10;

            /* do loop execution */
            do
            {
                if (a == 15)
                {
                    /* skip the iteration */
                    a = a + 1;
                    continue;
                }
                Console.WriteLine("value of a: {0}", a);
                a++;
            }
            while (a < 20);
            Console.ReadLine();
        }
    }
    }