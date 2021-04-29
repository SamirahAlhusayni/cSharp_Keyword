# `this ` keyword in C#
<div dir = "rtl"> 
يمكن استخدام الكلمة  this  في موضعين مختلفين الأول عندما يكون لديك نوع بيانات مخصص وهو  class  فانه عند استنساخ عدة  objects من هذا الكلاس فإنها تسمى  instance  في كل مرة يتم التعامل مع أي منها يشار لها في  class  بكلمة this.field or method والذي يعني تعامل مع البيانات أو العمليات الخاصة بهذا  object  الحالي، أما الموضع الثاني فهو عند عمل  extension method فإانه يتم وضع  this  أمام نوع المتغير المراد إلحاق هذه الدالة به في رأس تعريف الدالة.

الصيغة:
</div>

    this. field or opperation
<div dir = "rtl"> 
 مثال:

في هذا المثال تم استخدام كلمة  this  كمشير الى   الموظف الحالي وعند الرغبة في الوصول الى  الخصائص أو العمليات الخاصة بكل موظف داخل class فانه فقط يتم الوصول لها من خلال كلمة this 
</div>
<div dir = "ltr"> 

       public class Employee
    {
    private string alias;
    private string name;

    public Employee(string name, string alias)
    {
        
    
        this.name = name;
        this.alias = alias;
    }
    }
</div>