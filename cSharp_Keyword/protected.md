# `protected ` keyword in C#
<div dir = "rtl"> 
أحد Access modifires أو ما يعرف بمعدلات الوصول، يتم الوصول لها داخل النوع النفسه أو الأنواع التي ترث منه

الصيغة:
</div>

 `  class SampleClass
    {
    protected int x; 
    }`
<div dir = "rtl"> 
 مثال:
في هذا المثال تم استخدام protected ليصبح ممسموح الوصول له من الانواع الحالية مثل A أو الأنواع التي ترث من A مثل B
</div>
<div dir = "ltr"> 

   class A
{
    protected int x = 123;
}

    class B : A
    {
    static void Main()
    {
        var a = new A();
        var b = new B();
        b.x = 10;
    }
    }}

</div>