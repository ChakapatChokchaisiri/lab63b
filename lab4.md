# การทดลองที่๔ เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล

## วัตถุประสงค์
1. เพื่อให้มีความเข้าใจเกี่ยวกับการ input จากภายนอกเข้าไปใน microcontroller

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์

2. คอมพิวเตอร์

3. เซ็นเซอร์แสงที่มีตัวต้านทาน

## ศึกษาข้อมูลเบื้องต้น

https://www.youtube.com/watch?v=nFqoZT26U5k

## วิธีการทำการทดลอง

1. ใช้คำสั่ง _pwd_ และ _vi src/main.cpp_ เพื่อเรียกดู source code ของ input port

![image](https://user-images.githubusercontent.com/80879398/112196971-24e85900-8c3e-11eb-97b5-c4584f6443f1.png)

2. วิเคราะห์ source code

3. ใช้คำสั่ง _pio run -t upload_ 

![image](https://user-images.githubusercontent.com/80879398/112196977-26b21c80-8c3e-11eb-88aa-19012be99456.png)

4. เมื่อโปรแกรมขึ้นคำว่า Connecting ให้กดปุ่ม upload ค้างไว้และกดปุ่ม reset ที่ microcontroller

5. ใช้คำสั่ง _pio device monitor_

![image](https://user-images.githubusercontent.com/80879398/112196981-274ab300-8c3e-11eb-892f-e1c0586e743a.png)

6. สังเกตผลที่ได้จากการทดลอง

7. เมื่อนำเซ็นเซอร์แสงไฟต่อกับ microcontroller โดยให้ขาแรกต่อกับเซ็นเซอร์ และนำเซ็นเซอร์และตัวต้านทานต่อเข้ากับ port 0 และ นำขาอีกข้างต่อเข้ากับสายดิน 

![image](https://user-images.githubusercontent.com/80879398/112196983-274ab300-8c3e-11eb-9b20-23a21dad92c8.png)

8.นำสาย input ต่อเข้ากับเซ็นเซอร์ที่ port 0

![image](https://user-images.githubusercontent.com/80879398/112196985-27e34980-8c3e-11eb-9b33-bc0deb0fe4d9.png)

9.นำมือไปแตะเซ็นเซอร์เอามือออก

10.สังเกตุผลที่ได้จากการทดลอง

## การบันทึกผลการทดลอง

หน้าต่าง output ของ code ขึ้นคำว่า read 1 ขณะที่ microcontroller ไฟดับ

แต่เมื่อนำสายไฟไปจิ้มที่ port 0 หรือกดปุ่ม upload output ของ code ขึ้นคำว่า read 0 และ LED ที่ microcontroller จะมีไฟติด

![image](https://user-images.githubusercontent.com/80879398/112196987-287be000-8c3e-11eb-97f3-a31fb39206c2.png)

เมื่อนำนิ้วไปปิดเซ็นเซอร์ output ของ code ขึ้นคำว่า read 0 และ LED ที่ microcontroller จะมีไฟติด
แต่เมื่อนำนิ้วออกจากเซ็นเซอร์ หน้าต่าง output ของ code ขึ้นคำว่า read 1 ขณะที่ microcontroller ไฟดับ

## อภิปรายผลการทดลอง

จากโค้ดส่วน void setup คือการ setup ให้ port 0 และ 2 เป็น input และ output ตามลำดับ

จากโค้ดส่วน void loop เป็นการ setup loop ให้ port 2 เป็น high ถ้ามีกระแสเข้าที่ port 0

## คำถามหลังการทดลอง

เราสามารถนำการทดลองนี้ไปประยุกต์ใช้ในชีวิตประจำวันอย่างไร

- ใช้เซ็นเซอร์อุณหภูมืแทนเซนเซอร์แสง แล้วใช้ output แทน switch ใช้เปิดปิดเครื่องปรับอากาศเมื่อุณหภูมิสูงกว่าที่กำหนด
