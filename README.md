
1.Extract this to your XAMPP at path of  C:\xampp\htdocs

2.Create a database myblog_db import the SQL file

2.Run this http://localhost/Food-blog/public







NOTE!!! THIS IS A ERROR FOR ADDING A PICTURE DUE TO RESIZING IMAGE.

Fatal error: Uncaught Error: Call to undefined function imagecreatefromjpeg() in C:\xampp\htdocs\Food-blog\app\core\functions.php:311 Stack trace: #0 C:\xampp\htdocs\Food-blog\app\pages\admin\posts-controller.php(39): resize_image('uploads/1706907...') #1 C:\xampp\htdocs\Food-blog\app\pages\admin.php(30): require_once('C:\\xampp\\htdocs...') #2 C:\xampp\htdocs\Food-blog\public\index.php(19): require_once('C:\\xampp\\htdocs...') #3 {main} thrown in C:\xampp\htdocs\Food-blog\app\core\functions.php on line 311

If you get caught to this error situation of Attaching a Picture. 

You need set-up and download libjpeg. To download a php extension called libjpeg. Go to this (https://github.com/libjpeg-turbo/libjpeg-turbo/releases)


STEP 1: Find these name:


  libjpeg-turbo-3.0.2-gcc.exe: NOTE For 32bit Computers

	libjpeg-turbo-3.0.2-gcc64.exe: NOTE For 64bit Computers
 ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/d613ea58-ddf0-4ee8-a55f-125f7ece05af)


STEP 2: Execute the downloaded libjpeg-turbo-3.0.2-gcc64.exe executable file. This will initiate the extraction process.
	Upon completion, navigate to the extracted folder.


STEP 3:	Copy the DLL Files inside of the BIN : Open where you extracted the file and go to this. Ex. C:\libjpeg-turbo-gcc64\bin
	Within the extracted folder, locate the DLL files related to libjpeg-turbo, typically named jpeg62.dll or similar.
	Copy all those DLL files.
      ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/ff6fc369-fcc8-437a-829b-164e9d042790)

STEP 4: Go to your XAMPP Click the Config Module of the APACHE, then click <Browse> [PHP] A folder will appear. Find the ext named folder.
          ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/46a0b95d-42ec-4eca-bceb-b543b89fe816)

        here is the EXT 
        ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/f17288e0-a98d-4767-9da2-9acfbebc5aca)

STEP 5: Inside of the ext folder paste the DLL Files you copy.
          ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/bc201dff-7adc-475e-bffe-e0f531a34b92)

STEP 6: Go to your XAMPP Click the Config Module of the APACHE, then click the PHP (php.ini) A notepadd text will appear.
              ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/28faed85-e383-4c56-b50c-a78d1d7d299c)

STEP 7: On the notepad text of php.ini Hit CTRL + F and type this ;extension=gd Change it and add these two:
![image](https://github.com/Tactile4312/Food-blog/assets/114903179/0df2f56f-ff08-4b3a-9ef1-dbbca5872180)

	extension=gd
	extension=gd2
	Make sure you remove the semicolon so that the extension of php will be enabled.
![image](https://github.com/Tactile4312/Food-blog/assets/114903179/bf0edbbf-9cb2-47cd-9107-5a8a441d03ab)

	Then save the file.
 ![image](https://github.com/Tactile4312/Food-blog/assets/114903179/c22c3a96-1d45-4c2a-8f72-76ea05c4d5b1)

	
Restart the XAMPP and the Error will be gone.

	
