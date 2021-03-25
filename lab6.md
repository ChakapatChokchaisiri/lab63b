# การทดลองที่๖ เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)

## วัตถุประสงค์
1. เพื่อศึกษาเกี่ยวกับการทำ access point ของ wifi ไปยัง web server

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์
2. คอมพิวเตอร์

## ศึกษาข้อมูลเบื้องต้น

https://www.youtube.com/watch?v=T26DVHePlTs

## วิธีการทำการทดลอง
1.เชื่อมต่อ microcontroller เข้ากับคอมพิวเตอร์

2.ป้อนคำสั่ง _pwd_ และ _cd../06_wifi-ap-web-server_ ใน cmd เพื่อเข้าสู้โปรแกรมที่ 6 ของ microcontroller

3.ใช้คำสั่ง _vi src/main.cpp_ และศึกษา source code การทำงานของโปรแกรม

![image](https://user-images.githubusercontent.com/80879398/112250790-9bac4300-8c8c-11eb-982d-dc61f704be5c.png)

4.อัปโหลดโปรแกรมขึ้นไปบน microcontorller โดยใช้คคำสั่ง _pio run -t upload_

5.กดปุ่ม upload ค้างไว้และกดปุ่ม reset ที่ microcontroller ตามลำดับ

6.ใช้คำสั่ง _pio device monitor_ 

7.ทดสอบการค้นหา wifi และบันทุกผลที่ได้จากการทดลอง

## การบันทึกผลการทดลอง

มี wifi เกิดขึ้นในการค้นหา wifi ของอุปกณ์รับ wifi ภายในระยะของ microcontroller

![image](https://user-images.githubusercontent.com/80879398/112250613-42441400-8c8c-11eb-9cde-0be4357f91f7.png)

## อภิปรายผลการทดลอง

จากโค้ดส่วน ssid และ password เป็นการสร้างชื่อและรหัสของ wifi ที่ต้องการจะสร้าง

และโค้ดส่วน void setup คือการทำให้เกิดสัญญาณ wifi ในระยะ

## คำถามหลังการทดลอง

การเชื่อมต่อแบบ WiFi หมายถึงอะไร

- การเชื่อมต่อแบบไร้สายโดยมีการสื่อสารผ่านทางคลื่นวิทยุแทนการใช้สาย(แบบLAN)
