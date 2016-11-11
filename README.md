##นายเอกชัย  ภมรสุขนิรันดิ์  57030253
#ใบงานที่ 5
##เรื่อง การใช้งานคำสั่ง Console.WriteLine()
##วัตถุประสงค์
1). เพื่อให้นักศึกษาบอกวิธีการใช้คำสั่งแสดงผลบน Text Mode ในภาษา C# ได้
2). เพื่อให้นักศึกษาสามารถปรับแต่งคำสั่งแสดงผลทางหน้าจอตามต้องการได้

##ขั้นเตรียมการทดลอง
1). สร้าง Project ตั้งชื่อเป็น Lab5 เพื่อทดลองการใช้งานคำสั่ง Console.WriteLine()
ลำดับขั้นการทดลอง
(หมายเหตุ ในรูปประกอบที่มี namespace เป็น Lab4 รบกวนแก้เป็น Lab5 ด้วยครับ)
2). ทดลองเรื่องจำนวนของอาร์กิวเมนต์ในคำสั่ง Console.WriteLine()

 2.1). แก้โปรแกรมตามรูปด้านล่างนี้

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic1.png)

  2.2). รันโปรแกรม และบันทึกผลที่ได้
  ```
  using System;
namespace LAB5
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("This is text 1.");
            Console.WriteLine("This is text 2.");
            Console.WriteLine("This is text 3.");
        }
    }
}
  ```
![](https://github.com/Ekachai253/LAB-05/blob/c603ff5c5dd441d70a1eacc1786a2bbe9ee034a5/img/run.jpg)
#จากการรันโปรเเกรมพบว่า เป็นทำให้ขึ้นบรรทัดใหม่ ของข้อความ 1,2,3 
 2.3). แก้โปรแกรมตามรูปด้านล่างนี้
 
  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic2.png)

 2.4). รันโปรแกรม และบันทึกผลที่ได้
 ```
using System;
namespace LAB5
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("{0} and {1}.",3,6);
        }
    }
}
```
![](https://github.com/Ekachai253/LAB-05/blob/c603ff5c5dd441d70a1eacc1786a2bbe9ee034a5/img/run1.jpg)

#จากการรันโปรเเกรมพบว่า เป็นการเลือกข้อมูลในตำเเหน่งที่ข้อมูลอยู่ เช่น ดังโค้ดด้านล่าง ผลการรันจะได้ 9 and 88
```
using System;
namespace LAB5
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("{4} and {9}.",3,6,7,9,69,11,2,7,88);
        }
    }
}
```

###คำถาม 5.1 เครื่องหมาย { }  ในคำสั่ง Console.WriteLine() มีลักษณะการใช้งานอย่างไร

#เครื่องหมาย {} มีลักษณะการใช้งานคลายๆกับ %d %f ซึ่งมันจะดึงข้อมูลตัวข้างหลัง , มาเเสดง 

###คำถาม 5.2  ถ้ามีการใช้ตัวเลขใน { } ที่กระโดด เช่น {0} {2} {3} จะใช้งานได้หรือไม่ อย่างไร จงอธิบาย

#ใช้งานได้ เพราะ การที่เราใส่เลขไปในเครื่องหมาย{} จะเป็นการกำหนด ว่าเราจะนำข้อมูล ที่ตำเเหน่งไหนมาเเสดง เช่น Console.WriteLine("{2} and {3}.",3,6,7,9);
ผลการรันจะได้ 6 and 
 
 2.5). แก้โปรแกรมตามรูปด้านล่างนี้

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic3.png)

 2.6). รันโปรแกรม และบันทึกผลที่ได้
```
using System;
namespace LAB5
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("{1},{0} and {1}.", 3, 6);
        }
    }
}
```
![](https://github.com/Ekachai253/LAB-05/blob/290d3265491310ada190b948fd5bd93a53a28061/img/run2.jpg)
#จากการรันโปรเเกรมพบว่า Console.WriteLine("{1},{0} and {1}.", 3, 6); จะเลือกข้อมูลตำเเหน่งที่ 1,0,1 มาเเสดง

3). ทดลองเรื่องการกำหนดความกว้างของอาร์กิวเมนต์

  3.1). แก้โปรแกรมตามรูปด้านล่างนี้

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic4.png)

  3.2). รันโปรแกรม และบันทึกผลที่ได้
```
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("         11234567892");
            Console.WriteLine("12345678901234567890");
            Console.WriteLine("{0,0}", 1);
            Console.WriteLine("{0,1}", 1);
            Console.WriteLine("{0,2}", 1);
            Console.WriteLine("{0,3}", 1);
            Console.WriteLine("{0,5}", 1);
            Console.WriteLine("{0,10}", 1);
            Console.WriteLine("{0,15}", 1);
            Console.WriteLine("{0,20}", 1);
        }
    }
}
```
![](https://github.com/Ekachai253/LAB-05/blob/22b98bd72d391a9113b2711f6db6ba30877d8720/img/run3.jpg)
#จากการรันโปรเเกรมพบว่า เป็นการเลือกใช้ข้อมูล บิตที่ 1 ในตำเเหน่ง 0,1,2,3,5,10,15,20

###คำถาม 5.3 การกำหนดความกว้างของอาร์กิวเมนต์ด้วยเครื่องหมาย { , }  ในคำสั่ง Console.WriteLine() มีรูปแบบการใช้งานอย่างไร
#การกำหนดความกว้างของอาร์กิวเมนต์ด้วยเครื่องหมาย { , } มีรูปแบบการใช้งานเเบบเลือกข้อมูลเเละกำหนดตำเเหน่งสุดท้ายให้กับข้อมูล


4). ทดลองเรื่องการกำหนดรูปแบบของอาร์กิวเมนต์
  4.1). แก้โปรแกรมตามรูปด้านล่างนี้

  ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic5.png)

  4.2). รันโปรแกรม และบันทึกผลที่ได้
  ```
  using System;
namespace Lab5
{
    class Program
    {
        static void Main(string[] args)
        {
                int n = 123456789;
                Console.WriteLine("{0:E}", n);
                Console.WriteLine("{0:F}", n);
                Console.WriteLine("{0:G}", n);
                Console.WriteLine("{0:N}", n);
                Console.WriteLine("{0:P}", n);
                Console.WriteLine("{0:X}", n);
            
        }
    }
}
```
![](https://github.com/Ekachai253/LAB-05/blob/0c14bb130dd14b2cc46e42a6de0a4a9e243faf68/img/run4.jpg)

5). ทดลองเรื่องการกำหนดรูปแบบพร้อมความกว้างของอาร์กิวเมนต์
  5.1). แก้โปรแกรมตามรูปด้านล่างนี้
 
 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic6.png)

  5.2). รันโปรแกรม และบันทึกผลที่ได้
  ```
  using System;
namespace Lab5
{
    class Program
    {
        static void Main(string[] args)
        {
                int n = 123456789;
                Console.WriteLine("{0,20:E}", n);
                Console.WriteLine("{0,20:F}", n);
                Console.WriteLine("{0,20:G}", n);
                Console.WriteLine("{0,20:N}", n);
                Console.WriteLine("{0,20:P}", n);
                Console.WriteLine("{0,20:X}", n);
            
        
    }
}
    }

  ```
![](https://github.com/Ekachai253/LAB-05/blob/0c14bb130dd14b2cc46e42a6de0a4a9e243faf68/img/run5.jpg)

6). ทดลองเรื่องการกำหนดรูปแบบพร้อมความกว้างของทศนิยมของอาร์กิวเมนต์
  6.1). แก้โปรแกรมตามรูปด้านล่างนี้

 ![](https://github.com/Desktop-Programming-Lab-2559/LAB-05/blob/master/img/pic7.png)

  6.2). รันโปรแกรม และบันทึกผลที่ได้
  ```
  using System;
namespace Lab5
{
    class Program
    {
        static void Main(string[] args)
        {
                Console.WriteLine("{0:F1}", 123.456789);
                Console.WriteLine("{0:F2}", 123.456789);
                Console.WriteLine("{0:F3}", 123.456789);
                Console.WriteLine("{0:F4}", 123.456789);
                Console.WriteLine("{0:F5}", 123.456789);
            
        }
    }
}
```
![](https://github.com/Ekachai253/LAB-05/blob/0c14bb130dd14b2cc46e42a6de0a4a9e243faf68/img/run6.jpg)
#จากการรันโปรเเกรมพบว่า เป็นคำสั่งที่ใช่เลือกหลักทศนิยม

## แบบฝึกหัด จงระบุ output ของบรรทัดคำสั่งต่อไปนี้

```csharp
1.  string name = "Hello";
    Console.WriteLine(String.Format("{0} there. I said {0}! {0}???", name));
2.    Console.WriteLine("{2:d} {0:d} {1:d}", 1, 2, 3);
3.    Console.WriteLine("Hello " + "World");
4.    Console.WriteLine("Here comes a slash \\");
5.    Console.WriteLine("|{0, 10}|", 999);
6.    Console.WriteLine("|{0,-10}|", 000);
7.    Console.WriteLine("The value: {0}.", 500);
8.    Console.WriteLine("The value: {0:C}.", 500);
9.    Console.WriteLine("{0,-10:F4}", 12.3456789);
10.   Console.WriteLine("{0,-10:C}", 12.3456789);
11.   Console.WriteLine("{0,-10:E3}", 12.3456789);
12.   Console.WriteLine("{0,-10:x}", 65535);
13.   Console.WriteLine("{0,-10:X}", 65535);
14.   int i; 
      Console.WriteLine("Value\tSquared\tCubed"); 
      for(i = 1; i < 10; i++) 
          Console.WriteLine("{0}\t{1}\t{2}", i, i*i, i*i*i); 
15.    Console.WriteLine("{0:#.###}.", 1234.56789);
```

##ตอบ
```
using System;
namespace Lab5
{
    class Program
    {
        static void Main(string[] args)
        {
            string name = "Hello";
            Console.WriteLine(String.Format("{0} there. I said {0}! {0}???", name));
            Console.WriteLine("{2:d} {0:d} {1:d}", 1, 2, 3);
            Console.WriteLine("Hello " + "World");
            Console.WriteLine("Here comes a slash \\");
            Console.WriteLine("|{0, 10}|", 999);
            Console.WriteLine("|{0,-10}|", 000);
            Console.WriteLine("The value: {0}.", 500);
            Console.WriteLine("The value: {0:C}.", 500);
            Console.WriteLine("{0,-10:F4}", 12.3456789);
            Console.WriteLine("{0,-10:C}", 12.3456789);
            Console.WriteLine("{0,-10:E3}", 12.3456789);
            Console.WriteLine("{0,-10:x}", 65535);
            Console.WriteLine("{0,-10:X}", 65535);
            int i;
            Console.WriteLine("Value\tSquared\tCubed");
            for (i = 1; i < 10; i++)
            Console.WriteLine("{0}\t{1}\t{2}", i, i * i, i * i * i);
            Console.WriteLine("{0:#.###}.", 1234.56789);

        }
    }
}
```
![](https://github.com/Ekachai253/LAB-05/blob/0c14bb130dd14b2cc46e42a6de0a4a9e243faf68/img/run7.jpg)

