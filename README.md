Obfuscate Textfield module
--------------------------
By: Kevin Moll kevin.j.moll@gmail.com

This is a module created to hide the value of a textfield from the user.  
The primary use case for this module is on Admin forms where secrets or
 passwords are entered (ex, for 3rd party APIs or services).

It is meant to be a drop in replacement for a textfield.  Simply enable 
the module and change any form field #type to 'obfuscate_textfield'.

This form element was modeled after the file_managed form element. It works 
the same by showing you different markup '****' if there is a value, and 
adding a 'Change' button.  It works differently from the file_managed element 
in that it saves the values as the top level element rather than saving it 
as an array.  This is necessary to make this a drop in replacement for a textfield.

@TODO
-----
Integrate with Encryption API and support an #encrypt element property.  
**Note, that since this is meant to work with Admin forms, which saves all values 
as variables, we can encrypt the value when setting it, but it would be up to the 
user to decrypt the value when it is used in code.
