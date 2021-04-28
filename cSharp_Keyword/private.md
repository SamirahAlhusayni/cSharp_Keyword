# `private ` keyword in C#
<div dir = "rtl"> 
أحد Access modifires أو ما يعرف بمعدلات الوصول، تعتبر أكثر المعدلات تفرض قيود بالتالي الوصول لها يصبح صعب، لا يتم الوصول لها الا داخل النوع نفسه، واذا لم توضع يتم وضع النوع مباشرة يفترضه private

الصيغة:
</div>

 `class SampleClass
    {
    private int x; 
}`
<div dir = "rtl"> 
 مثال:
في هذا المثال تم إنشاء نوع بيانات باسم Employee2 وتم تعريف  fields له باستخدام المعدل private والذي يفرض قيود على من يلتحق به فلا يظهر الا في النوع الحالي فقط ولا يتم التواصل معه من قبل الأنواع الاخرى والذي سيتم الوصول له من أي نقطة في البرنامج.
 
</div>
<div dir = "ltr"> 

    class Employee2
    {
    private string name = "FirstName, LastName";
    private double salary = 100.0;

    public string GetName()
    {
        return name;
    }

    public double Salary
    {
        get { return salary; }
    }
    }

    class PrivateTest
    {
    static void Main()
    {
        var e = new Employee2();


        string n = e.GetName();

        double s = e.Salary;
    }
    }

</div>