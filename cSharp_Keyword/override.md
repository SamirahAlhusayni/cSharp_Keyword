# `override ` keyword in C#
<div dir = "rtl"> 
أحد Inheritance modifires أو ما يعرف بمعدلات الوراثة، عندما يتم كتابتها في تعريف الـ method  داخل sub class  فإن هذا يعني أن هذا النوع الوارث يستطيع التعديل في تنفيذ هذه الـ method طالما أنه كتب أمام هذه الـ method  المعدل virtual في الـ super class 


الصيغة:
</div>

 `public override int higth() {}`
<div dir = "rtl"> 
 مثال:
 في هذا المثال تم تعريف نوع أساسي بمسمى Shape وهو الشكل الذي قد يكون دائرة أو مربع أو غيرها، لذلك تم تعريف أنواع أخرى ترث من هذا النوع مثل Sphere و Circle ولديها method لحساب المساحة لكل شكل على حدة بطريقة تعتمد على معادلة حساب مساحة  هذا الشكل بالتالي تكون اختلفت في التنفيذ فكانت كلمتي virtual و  override هي الحل المناسب في إمكانية تطبيق آلية تنفيذ مختلفة حسب النوع والسياق ولكن لنفس الـ  method ويتم التعرف عليها فقط من نوع object  الذي قام باستدعائها.
</div>
<div dir = "ltr"> 

    class TestClass
    {
    public class Shape
    {
        public const double PI = Math.PI;
        protected double x, y;

        public Shape()
        {
        }

        public Shape(double x, double y)
        {
            this.x = x;
            this.y = y;
        }

        public virtual double Area()
        {
            return x * y;
        }
    }

    public class Circle : Shape
    {
        public Circle(double r) : base(r, 0)
        {
        }

        public override double Area()
        {
            return PI * x * x;
        }
    }

    class Sphere : Shape
    {
        public Sphere(double r) : base(r, 0)
        {
        }

        public override double Area()
        {
            return 4 * PI * x * x;
        }
    }

    class Cylinder : Shape
    {
        public Cylinder(double r, double h) : base(r, h)
        {
        }

        public override double Area()
        {
            return 2 * PI * x * x + 2 * PI * x * y;
        }
    }

    static void Main()
    {
        double r = 3.0, h = 5.0;
        Shape c = new Circle(r);
        Shape s = new Sphere(r);
        Shape l = new Cylinder(r, h);
        // Display results.
        Console.WriteLine("Area of Circle   = {0:F2}", c.Area());
        Console.WriteLine("Area of Sphere   = {0:F2}", s.Area());
        Console.WriteLine("Area of Cylinder = {0:F2}", l.Area());
    }
    }
</div>