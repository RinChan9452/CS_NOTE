**First session**

***Start Page***
* เช็คว่า user จะทำการ login หรือ sign in 
* ปุ่ม login จะ link ไปหน้า login interface
* ปุ่ม sign in จะ link ไปหน้า register interface

***Register interface***
* รับ name-surname -> email -> phone number -> username -> password -> confirm password
* รอเช็คว่าจะแยกหน้าหรือไม่


***login interface***
* สร้างหน้า login สำหรับใส่ username และ password
* login เสร็จจะเข้าหน้า user interface ที่จะแตกต่างกันตาม authority ซึ่งแบ่งเป็น admin, officer, user โดยจะใช้ switch case ในการ switch ไปหน้า interface ที่ตนเองเข้าถึงได้

Note: Authority (3 ระดับ) \
|—– 0 = user\
|—– 1 = officer\
|—– 2 = admin


***user interface***
* ในหน้า user interface จะสามารถมีการเปลี่ยนรูป profile ผ่าน logo ซ้ายบน โดยเมื่อ click เข้าจะ link ไปที่หน้า profile change interface 
* การเปลี่ยนรหัสจะสามารถทำได้ในหน้า user interface ผ่านปุ่ม change your password โดยตัวปุ่มจะ link ไปที่ change password interface โดย new password จะทำการ setPassword รหัสเก่าเพื่อทำการเปลี่ยนรหัส

Note: this.password = newPassword;