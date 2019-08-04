CapGen 
=================

It is a simple PHP program to generate captcha for form validation. It can be integrated in any website for captcha generation. This project is based on converting text to image using PHP with help of GD. It obtains 4 characters and insert them in an image.

Silent Features 
================
* Each 4 character have different font , random font from the set of 10 fonts. 
* Each character has different colour, font size, orientation and position 
* Final captcha has many lines with different orientation, size, position and colour.<br>
![g](/screenshot/img0.png)  ![g](/screenshot/img1.png)

Installation
================
* Clone this repository:  
```console
git clone https://github.com/skshivam64/fZend.git
```
or click `Download ZIP` in the right panel of repository and extract it.
* Copy `captcha-generator` folder into the project directory.
* Copy this line to HTML or PHP file of the project.
```html
<div id="ae_captcha_api"></div>
```
* Copy this script import line at the bottom of the body of same HTML or PHP file.
```html
<script src="./captcha-generator/asset/main.js"></script>
```
Validating captcha 
===================
* Create a form with a `Text Field` and `Button` to send the user input to server using `POST` method.
* On server side use session variable `$_SESSION['secure']` for validating captch. For example:
```php
if($_SESSION['secure'] == $_POST['user_input']){
  echo "captcha validated.";
} 
else{
  echo "captcha validation failed.";
}
```
---------------------------------------------
