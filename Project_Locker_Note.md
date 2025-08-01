**First session**

***Start Page***
* เช็คว่า user จะทำการ login หรือ sign in 
* ปุ่ม login จะ link ไปหน้า Login Interface
* ปุ่ม sign in จะ link ไปหน้า Register interface

***Register Interface***
* รับ name-surname -> email -> phone number -> username -> password -> confirm password
* เมื่อ register เสร็จจะทำการ link ไปที่หน้า login


***login Interface***
* สร้างหน้า login สำหรับใส่ username และ password
* มีปุ่ม sign in ในการเข้าหน้า register เผื่อ user กดผิดหรือคิดว่ามี account อยู่แล้ว
* หาก username หรือ password ผิดจะไม่ทำการ link ไปหน้า User Interface
* หาก username และ password เป็น account ที่ถูก ban จะไม่สามารถ login ผ่านไปได้
* login เสร็จจะเข้าหน้า User Interface ที่จะแตกต่างกันตาม authority ซึ่งแบ่งเป็น admin, officer, user โดยจะใช้ switch case ในการ switch ไปหน้า interface ที่ตนเองเข้าถึงได้

Note: Switch Case Authority (3 ระดับ) \
|—– 0 = user\
|—– 1 = officer\
|—– 2 = admin

Note: หลัง officer ทำการ login จะเข้าสู่หน้า Change Password Interface อัตโนมัติเพื่อให้เปลี่ยนรหัสผ่านก่อนที่จะสามารถเข้าสู่หน้า User Interface ได้

***User Interface***
* ในหน้า User Interface จะสามารถเปลี่ยนรูป profile ผ่าน logo ซ้ายบน โดยเมื่อ click เข้าจะ link ไปที่หน้า profile change interface 
* option ในหน้า user interface นี้จะแตกต่างกันออกไปตาม authority ของตัว user


***Change Password Interface***
* การเปลี่ยนรหัสจะสามารถทำได้ในหน้า user interface ผ่านปุ่ม change your password โดยตัวปุ่มจะ link ไปที่ change password interface โดย new password จะทำการ setPassword รหัสเก่าเพื่อทำการเปลี่ยนรหัส

Note: this.password = newPassword;

***Profile Change Interface***