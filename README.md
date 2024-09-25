- 👋 Hi, I’m @Fangyada
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Fangyada/Fangyada is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<?php
$servername = "localhost";
$username = "root";
$password = "yourpassword"; //ถ้าไม่ได้ตั้งรหัสผ่านให้ลบ yourpassword ออก
 
try {
  $conn = new PDO("mysql:host=$servername;dbname=workshop_pdo;charset=utf8", $username, $password);
  // set the PDO error mode to exception
  $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
  //echo "Connected successfully";
} catch(PDOException $e) {
  echo "<?php 
if(isset($_GET['id'])){
require_once 'connect.php';
//ประกาศตัวแปรรับค่าจาก param method get
$id = $_GET['id'];
$stmt = $conn->prepare('DELETE FROM tbl_member WHERE id=:id');
$stmt->bindParam(':id', $id , PDO::PARAM_INT);
$stmt->execute();
 
//  sweet alert 
echo '
    <script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert-dev.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert.css">';
 
  if($stmt->rowCount() ==1){
        echo '<script>
             setTimeout(function() {
              swal({
                  title: "ลบข้อมูลสำเร็จ",
                  type: "success"
              }, function() {
                  window.location = "index.php"; //หน้าที่ต้องการให้กระโดดไป
              });
            }, 1000);
        </script>';
    }else{
       echo '<script>
             setTimeout(function() {
              swal({
                  title: "เกิดข้อผิดพลาด",
                  type: "error"
              }, function() {
                  window.location = "index.php"; //หน้าที่ต้องการให้กระโดดไป
              });
            }, 1000);
        </script>';
    }
$conn = null;
} //isset
?> failed: " . $e->getMessage


6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
<?php 
if(isset($_GET['id'])){
require_once 'connect.php';
//ประกาศตัวแปรรับค่าจาก param method get
$id = $_GET['id'];
$stmt = $conn->prepare('DELETE FROM tbl_member WHERE id=:id');
$stmt->bindParam(':id', $id , PDO::PARAM_INT);
$stmt->execute();
 
//  sweet alert 
echo '
    <script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert-dev.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert.css">';
 
  if($stmt->rowCount() ==1){
        echo '<script>
             setTimeout(function() {
              swal({
                  title: "ลบข้อมูลสำเร็จ",
                  type: "success"
              }, function() {
                  window.location = "index.php"; //หน้าที่ต้องการให้กระโดดไป
              });
            }, 1000);
        </script>';
    }else{
       echo '<script>
             setTimeout(function() {
              swal({
                  title: "เกิดข้อผิดพลาด",
                  type: "error"
              }, function() {
                  window.location = "index.php"; //หน้าที่ต้องการให้กระโดดไป
              });
            }, 1000);
        </script>';
    }
$conn = null;
} //isset
?>
ผลการทำงาน


 

ลองเอาตัวอย่างโค้ดไปรันและต่อยอดนะครับ ^^
แหล่งศึกษาเพิ่มเติม : https://websitebeaver.com/php-pdo-vs-mysqli
List of PDOStatement::bindParam data_type parameters : https://www.php.net/manual/en/pdo.constants.php

ขายโปรแกรม ลดสูงสุด 70%
ขายระบบสารสนเทศออนไลน์ พร้อมใช้ ราคาเบาๆ ได้โค้ดทั้งหมด นำไปต่อยอดได้
สินค้าทั้งหมด คลิก  https://devbanban.com/?p=4425
ซื้อแล้วปรึกษาได้เรื่อยๆ ครับ
สนใจ inbox มาที่แฟนเพจ หรือ ☎️ 0948616709

ร่วมสนับสนุน ค่ากาแฟ ค่าโฮส devbanban.com ได้ที่

ธนาคารกรุงไทย สาขาเดอะมอลล์ท่าพระ
ชื่อบัญชี นายพิศิษฐ์  บวรเลิศสุธี   เลขที่  878-0-17747-6
————————————————————————————
ธนาคารไทยพาณิชย์ สาขามหาวิทยาลัยราชภัฏธนบุรี
ชื่อบัญชี นายพิศิษฐ์  บวรเลิศสุธี เลขที่ 406-359094-1

fanpage : https://www.facebook.com/sornwebsites/

Share this:
Click to share on Facebook (Opens in new window)Click to share on X (Opens in new window)
Related

แจกโค้ด Sweet Alert Automatically Redirecting ไม่ต้องคลิก OK !!
In "PHP"


PHP แจกฟรีเว็บแคตตาล็อกสินค้า, สินค้าออนไลน์
In "PHP"


PHP PDO Display data in Checkbox Workshop แสดงและเลือกภาษาที่ชอบ
In "PDO"

Post navigation
PHP แปลงปี ค.ศ. เป็น พ.ศ. 
 PHP PDO : ตัวอย่างระบบอัพโหลดภาพ, Basic Upload Image



Related Post
PDOPHP
ฟรีคลิปสอนทำเว็บไซต์ PHP PDO MySQL AdminLTE3 2024
 Sep 2, 2024
PDOPHP
ระบบหอพัก , อพาร์ทเม้นท์ รายวัน รายเดือน ราคาเบาๆ เอาไปต่อยอดได้ 2024
 Aug 30, 2024
PHP
แจกขอบเขตระบบร้านตัดผม Barber Online System
 Jul 9, 2024
Search
Search
Top Posts
แจกตัวอย่าง Code PHP PDO MySQL CRUD  ระบบเพิ่ม ลบ แก้ไข แสดงข้อมูล เบื้องต้น, สอนทำเว็บแจกตัวอย่าง Code PHP PDO MySQL CRUD ระบบเพิ่ม ลบ แก้ไข แสดงข้อมูล เบื้องต้น, สอนทำเว็บ
โปรแกรมลดสูงสุด 70%  ได้โค้ดทั้งหมด  นำไปต่อยอดได้ทันทีโปรแกรมลดสูงสุด 70% ได้โค้ดทั้งหมด นำไปต่อยอดได้ทันที
PHP PDO  ระบบ Login - Logout ตรวจสอบสิทธิ์การใช้งานหน้าเว็บPHP PDO ระบบ Login - Logout ตรวจสอบสิทธิ์การใช้งานหน้าเว็บ
การนำ Google Font ไทย มาใช้งานในเว็บไซต์, ฟรี เพิ่มฟอนต์หน้าเว็บการนำ Google Font ไทย มาใช้งานในเว็บไซต์, ฟรี เพิ่มฟอนต์หน้าเว็บ
PHP แจกฟรีเว็บแคตตาล็อกสินค้า, สินค้าออนไลน์PHP แจกฟรีเว็บแคตตาล็อกสินค้า, สินค้าออนไลน์
สอนทำระบบแจ้งซ่อมออนไลน์ ฟรี, Helpdesk Systemสอนทำระบบแจ้งซ่อมออนไลน์ ฟรี, Helpdesk System
Fanpage


You missed
PDOPHP
ฟรีคลิปสอนทำเว็บไซต์ PHP PDO MySQL AdminLTE3 2024
 02/09/2024 พิศิษฐ์ บวรเลิศสุธี
PDOPHP
ระบบหอพัก , อพาร์ทเม้นท์ รายวัน รายเดือน ราคาเบาๆ เอาไปต่อยอดได้ 2024
 30/08/2024 พิศิษฐ์ บวรเลิศสุธี
BootstrapFree Template
แจกฟรี To-do list Ui ออกแบบจาก Bootstrap v5.3
 29/08/2024 พิศิษฐ์ บวรเลิศสุธี
PHP
แจกขอบเขตระบบร้านตัดผม Barber Online System
 09/07/2024 พิศิษฐ์ บวรเลิศสุธี
 
Proudly powered by WordPress | Theme: Newsup by Themeansar.

ขายระบบ
 
PHP
 
SQL
 
Bootstrap
 
Codeigniter
 
YouTube
 
สนับสนุน
 
มารู้จักกัน
// checks if INPUT_CONTEXT has just been released
// assumes `using static CitizenFX.Core.API;`
if(IsControlJustReleased(0, 51))
{
   // run code here 
}<?php 
if(isset($_GET['id'])){
require_once 'connect.php';
//ประกาศตัวแปรรับค่าจาก param method get
$id = $_GET['id'];
$stmt = $conn->prepare('DELETE FROM tbl_member WHERE id=:id');
$stmt->bindParam(':id', $id , PDO::PARAM_INT);
$stmt->execute();
 
//  sweet alert 
echo '
    <script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert-dev.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/1.1.3/sweetalert.css">';
 
  if($stmt->rowCount() ==1){
        echo '<script>
             setTimeout(function() {
              swal({
                  title: "ลบข้อมูลสำเร็จ",
                  type: "success"
              }, function() {
                  window.location = "index.php"; //หน้าที่ต้องการให้กระโดดไป
              });
            }, 1000);
        </script>';
    }else{
       echo '<script>
             setTimeout(function(startown) {
              swal({
                  title: "เกิดข้อผิดพลาด",
                  type: "error"
              }, function(dowtown,fivem,discord) {
                  window.location = "index.php"; //หน้าที่ต้องการให้กระโดดไป
              });
            }, 1000);
        </script>';
    }
$conn = null;
} //isset
?>

</a>


