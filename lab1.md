# การทดลองที่๑

## วัตถุประสงค์
1. เพื่อให้เข้าใจการทำงานและการเชื่อมต่อเบื้องต้นของ microcontroller

2. เพื่อศึกษาเกี่ยวกับการ run microcontroller

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์ ESP 01

2. คอมพิวเตอร์

## ศึกษาข้อมูลเบื้องต้น

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

## วิธีการทำการทดลอง

1.เชื่อมต่อ microcontrollerกับคอมพิวเตอร์ โดยการต่อUSBเพื่อไปยังserial และต่อserialเข้ากับmicrocontroller

2.เปิดหน้าต่าง cmd และใช้คำสั่ง _cd (ชื่อโฟล์เดอร์ที่มีโปรแกรม)_ และ _1s_
![image](https://user-images.githubusercontent.com/80879398/112188705-cc14c280-8c35-11eb-9cc0-8bbcbc0a76a7.png)

3.ใช้คำสั่ง _cd 01_Serial-Monitor_ ตามด้วย _visrc/main_ เพื่อดูและศึกษาโค้ดตัวอย่างโปรแกรมที่ใช้ทดสอบ microcontroller
![image](https://user-images.githubusercontent.com/80879398/112188711-cdde8600-8c35-11eb-963c-e86526177449.png)

4.ใช้คำสั่ง _vi platformio.ini_ เพื่อให้ทราบข้อมูลเบื้องต้นเกี่ยว microcontroller ที่นำมาใช้
![image](https://user-images.githubusercontent.com/80879398/112188715-ce771c80-8c35-11eb-9838-ebb086789e05.png)

5.ใช้คำสั่ง _pio run -t upload_ เพื่อเริ่ม run microcontroller
![image](https://user-images.githubusercontent.com/80879398/112188717-cfa84980-8c35-11eb-8fc7-5f0304fc0698.png)

6.กดปุ่มที่ microcontroller และกดปุ่ม set เพื่อให้microcontroller รับคำสั่งใหม่

7.เมื่อขึ้น success ให้ใช้คำสั่ง _pio device monitor_
![image](https://user-images.githubusercontent.com/80879398/112188726-d2a33a00-8c35-11eb-85e0-dfb513fcb309.png)
8.สังเกตุผลที่ได้จากการทดลอง

## การบันทึกผลการทดลอง

โปรแกรมมี output ออกมาเป็นเลขแบบ count โดยมีการ count เพิ่มทุก ๆ 1วินาที ตามที่โปรแกรมได้ถูกเขียนไว้ 

## อภิปรายผลการทดลอง

%%%%%%%%%%%%%%%%%%%%%%%%%%

## คำถามหลังการทดลอง

หากต้องการเปลี่ยนเป็นการ count ทุก ๆ 2วินาที ต้องแก้โค้ดส่วนใดอย่างไร

- แก้โปรแกรมในส่วนของ _void loop_ จาก _delay(1000)_ เป็น _delay(2000)_
