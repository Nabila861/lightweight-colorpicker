# lightweight-colorpicker
This is a lightweight and intuitive jQuery plugin, bringing a sleek Photoshop-style color picker to your web applications. It seamlessly integrates and enhances your color selection process, supporting RGB, HSB, and HEX formats. This repository houses modifications for improved user experience, streamlining color selection without any hassles.

## Basic Usage:

## Include jQuery:

Make sure to include the latest version of jQuery in your web page.
```html
<script type="text/javascript" src="jqueryLibrary.js"></script>
```
-----------------------------------------------------------------------------
## After including jQuery, add the Colpick Color Picker scripts and styles.

```html
<script type="text/javascript" src="colourpicker.js" ></script>
```          

## How to Include CSS

To utilize the Colpick styles, make sure you include the `colpick.css` in your project. 

```html
<link rel="stylesheet" href="path_to_your_styles_directory/colpick.css" type="text/css"/>
```

--------------------------------------------------------------------------
## Initialize the Plugin:

$('#picker').colpick();

## Example code of an input field changing with colour (mainly for Joget DX-8 form designs):
```html
<script type='text/javascript' src='#appResource.jqueryLibrary.js'></script>
<script src="#appResource.colourpicker.js#" type="text/javascript"></script>
<link rel="stylesheet" href="#appResource.colpick.css#" type="text/css"/>

<script type='text/javascript'>
    $(document).ready(function() {
        var field = FormUtil.getField("color_picker");

        $(field).colpick({
            submit: false, // this line removes the submit button
            onChange:function(hsb,hex,rgb,el) {
                $(el).css('background-color', '#' + hex); // Change background of the field itself
            },
            onHide:function(el){
                $(el).colpickSetColor($(el).css('background-color'));
            }
        });
    });
</script>
```
[Please do not forget to replace the src with your url or hash identifier]

-------------------------------------------------------------------------
## Options and Defaults:
The plugin comes with a wide range of options for customization. 
-------------------------------------------------------------------------

## Original Author and License:
The original Colpick Color Picker was developed by  josedvq. Please visit https://www.jqueryscript.net/other/Lightweight-jQuery-Color-Picker-For-Web-App-Colpick-Color-Picker.html for a more detailed execution.


