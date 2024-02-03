
1.Extract this to your XAMPP at path of  C:\xampp\htdocs

2.Create a database myblog_db import the SQL file

2.Run this http://localhost/Food-blog/public







NOTE!!! THIS IS A ERROR FOR ADDING A PICTURE DUE TO RESIZING IMAGE.

Fatal error: Uncaught Error: Call to undefined function imagecreatefromjpeg() in C:\xampp\htdocs\Food-blog\app\core\functions.php:311 Stack trace: #0 C:\xampp\htdocs\Food-blog\app\pages\admin\posts-controller.php(39): resize_image('uploads/1706907...') #1 C:\xampp\htdocs\Food-blog\app\pages\admin.php(30): require_once('C:\\xampp\\htdocs...') #2 C:\xampp\htdocs\Food-blog\public\index.php(19): require_once('C:\\xampp\\htdocs...') #3 {main} thrown in C:\xampp\htdocs\Food-blog\app\core\functions.php on line 311

If you get caught to this error situation of Attaching a Picture. 

You need set-up and download libjpeg. To download a php extension called libjpeg. Go to this (https://github.com/libjpeg-turbo/libjpeg-turbo/releases)

Find these name:

STEP 1: libjpeg-turbo-3.0.2-gcc.exe: NOTE For 32bit Computers

	libjpeg-turbo-3.0.2-gcc64.exe: NOTE For 64bit Computers

STEP 2: Execute the downloaded libjpeg-turbo-3.0.2-gcc64.exe executable file. This will initiate the extraction process.
	Upon completion, navigate to the extracted folder.

STEP 3:	Copy the DLL Files inside of the BIN : Open where you extracted the file and go to this. Ex. C:\libjpeg-turbo-gcc64\bin
	Within the extracted folder, locate the DLL files related to libjpeg-turbo, typically named jpeg62.dll or similar.
	Copy all those DLL files.

STEP 4: Go to your XAMPP Click the Config Module of the APACHE, then click <Browse> [PHP] A folder will appear. Find the ext named folder.

STEP 5: Inside of the ext folder paste the DLL Files you copy.

STEP 6: Go to your XAMPP Click the Config Module of the APACHE, then click the PHP (php.ini) A notepadd text will appear.

STEP 7: On the notepad text of php.ini Hit CTRL + F and type this ;extension=gd Change it and add these two:
	extension=gd
	extension=gd2
	Make sure you remove the semicolon so that the extension of php will be enabled.
	Then save the file.
	
Restart the XAMPP and the Error will be gone.

	