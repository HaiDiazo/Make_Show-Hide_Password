# Make Show/Hide Password
This is my script for make a button click and show/hide a text password. In my script, i use a boostrap 4.5 version, jquery 3.5.1, and font-awesome for the icon eye slash.

<div align="center">
<img src="https://user-images.githubusercontent.com/70514099/132086558-10dec842-051f-4cdd-87f6-568d5889b180.png">
    <p>Hide Password</p>
<img src="https://user-images.githubusercontent.com/70514099/132086717-d2bc6046-f059-41e5-863b-c422d896d13c.png">
    <p>Show Password</p>
</div>

## What i use
- [Boostrap] (https://getbootstrap.com/)
- [Jquery 3.5.1] (https://jquery.com/download/)
- [Font Awesome from W3schools] (https://www.w3schools.com/icons/icons_reference.asp)

## Getting Started
- First, you need add in head html. Required use jquery, but if you have your own css and font awesome. You don't need to add boostrap and font awesome.
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```
- Second, you need make a span text or button and input form with type password with name and id for variable javascript.
```html
<div class="form-group">
    <label for="Password" class="d-flex justify-content-between">
        <div>
            Password
        </div>
        <div class="pt-1">
          <span toggle="Password" id="toggle-password" class="fa fa-eye" style="font-size: 15px;"> show</span>
        </div>
    </label>
    <input type="password" class="form-control" name="password" id="Password" placeholder="" oninput="FilledData('Password')">
        <div id="alertPassword" class="hidden">
            <span class="text-danger font-italic">
                *please input your password
            </span>
        </div>
</div>
```
- Add id in tag span for initialization with javascript.
- Then, add script javascript in below.
```js
$('#toggle-password').on('click', function() {

            let input = $("#" + $(this).attr('toggle'));
            if (input.attr('type') == "password") {
                $(this).html(" hide");
                $(this).removeClass('fa fa-eye');
                $(this).addClass('fa fa-eye-slash');
                input.attr('type', 'text');
            } else {
                $(this).html(" show");
                $(this).removeClass('fa fa-eye-slash');
                $(this).addClass('fa fa-eye');

                input.attr('type', 'password')
            }
        });
```
- Done.


