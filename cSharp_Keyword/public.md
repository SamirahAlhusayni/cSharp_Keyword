# `public ` keyword in C#
<div dir = "rtl"> 
أحد Access modifires أو ما يعرف بمعدلات الوصول، تعتبر أكثر المعدلات تساهلا في الوصول فلا يوجد قيود للوصول إلى Data or Operation 
التي تكتب هذه الكلمة الى جانبها.  
فيتم الوصول لها سواء في هذا النوع أو الانواع التي ترث أو من أي نقطة أخرى داخل هذا البرنامج.


الصيغة:
</div>

 `class SampleClass
    {
    public int x; 
}`
<div dir = "rtl"> 
 مثال:
في هذا المثال تم إنشاء نوع بيانات باسم PointTest وتم تعريف  fields له باستخدام المعدل public والذي سيتم الوصول له من أي نقطة في البرنامج.
 
</div>
<div dir = "ltr"> 

    class PointTest
    {
    public int x;
    public int y;
    }

    class Program
    {
    static void Main()
    {
        var p = new PointTest();
    
        p.x = 10;
        p.y = 15;
        Console.WriteLine($"x = {p.x}, y = {p.y}");
    }
    }

</div>