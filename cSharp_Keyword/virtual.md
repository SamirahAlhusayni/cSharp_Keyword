# `virtual ` keyword in C#
<div dir = "rtl"> 
أحد Inheritance modifires أو ما يعرف بمعدلات الوراثة، عندما يتم كتابتها في تعريف الـ method  داخل الـ class فإن هذا يعني أنه بإمكان جميع الأنواع التي ترث من النوع الحالي أن تستخدم هذه  الـ method  كما تم تعريفها في النوع الرئيسي مع وجود إمكانية  تعديلها عند الرغبة في ذلك. 
  
تكتب في داخل base class method كتهيئة بأنه بالامكان التعديل عليها من قبل الأنواع التي سترث.
الصيغة:
</div>

 `public virtual int higth() {}`
<div dir = "rtl"> 
 مثال:
كما يظهر في هذا المثال تم تعريف نوع جديد من نوع base_class حتى تظهر كلمة vertual، , وهذا يعني نه بالامكان عليها من جميع من يرث منها
</div>
<div dir = "ltr"> 

    class base_class
    {
    public virtual void test();
    }

</div>