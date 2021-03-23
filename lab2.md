# การทดลองที่๒

## วัตถุประสงค์
1. เพื่อเรียนรู้วิธีการใช้ microcontroller เชื่อมต่อกับ wifi ได้อย่างถูกต้อง

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์

2. คอมพิวเตอร์

## ศึกษาข้อมูลเบื้องต้น

https://www.youtube.com/watch?v=yBjab0UNuB8

## วิธีการทำการทดลอง

1.เชื่อมต่อ microcontroller เข้ากับคอมพิวเตอร์โดยใช้ serial port

2.เปิด cmd และรันคำสั่ง _1s_ และ _vi src/main.cpp_


![image](https://user-images.githubusercontent.com/80879398/112192091-3e3ad680-8c39-11eb-8828-70c6cff2d4de.png)

3.ศึกษาการทำงานของโค้ดการค้นหา wifi

![image](https://user-images.githubusercontent.com/80879398/112192096-3f6c0380-8c39-11eb-8e3b-2a28213fcfa1.png)

4.รันคำสั่ง pio run -t upload

![image](https://user-images.githubusercontent.com/80879398/112192100-40049a00-8c39-11eb-8864-beecb60833c8.png)

5.เมื่อโปรแกรมขึ้นคำว่า _Connecting_ ให้กดปุ่ม upload ค้างไว้และกดปุ่ม reset ที่ microcontroller

6.รอโปรแกรม upload เสร็จสิ้นและใช้คำสั่ง _pio device monitor_ 

![image](https://user-images.githubusercontent.com/80879398/112192108-41ce5d80-8c39-11eb-8274-5076c34df410.png)

## การบันทึกผลการทดลอง

โปรแกรมได้มีการค้นหา wifi ที่อยู่ภายในระยะสัญญาณ

## อภิปรายผลการทดลอง

จากโค้ดส่วน void setup เป็นการเริ่มเต้น setup โปรแกรมเริ่มต้น

จากโค้ดส่วน void loop เป็นการวนลูปค้นหา wifi ซ้ำ ๆ 

## คำถามหลังการทดลอง

ถ้าบริเวณที่ทำการทดลองไม่มีสัญญาณ wifi โปรแกรมจะมีการแสดงผลอย่างไร
- NO NETWORK FOUND
