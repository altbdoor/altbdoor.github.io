---
layout: default
title: "Python And Notepad Plus Plus "
permalink: pages/python-and-notepad-plus-plus/
---

Python And Notepad Plus Plus 
===

*Archived from [This Is Monked](http://thisismonked.blogspot.com/2013/07/python-and-notepad-plus-plus.html), dated 20 July 2013.*

Yeah... So, this post is gonna teach you<br>
How to use [Notepad++](http://notepad-plus-plus.org/) with [Python](http://www.python.org/)

I've taken up Artificial Intelligence this semester<br>
While it is not compulsory, the lecturer taught Python<br>
So I picked it up for my second assignment<br>
The lecturer recommended an IDE of sorts<br>
But it was rather large and sluggish<br>
So I reverted to a pure Python setup<br>
Being an avid Notepad++ user, I wanted to use Python with it<br>
Turns out that it wasn't really easy

Of course, firstly, you would need the setup files for [Notepad++](http://notepad-plus-plus.org/download/) and [Python](http://www.python.org/download/)<br>
I will be using Python 2.7.5, but I believe its about the same for Python 3.x

The main function you would need is of course, compile<br>
You could set the PATH environment and call `python` every time<br>
But that would be tedious, so why not call it from Notepad++?<br>
If you don't know, Notepad++ can run files in many other programs

<img class="img" src="https://lh5.googleusercontent.com/-UrG1_cJSDeA/UeqeASe0LDI/AAAAAAAAA_0/0faxEW_hdEc/s1600/Untitled.png">

So, we'll be trying to get a "Run with Python" command in there<br>
First, we'll need to make a few preparations with Python

Your Python installation directory may vary<br>
I defaulted it to `C:\Python27\`<br>
Inside the directory, create a `.bat` file, and name it `python.bat`<br>
You are free to name it as anything, as long as you remember it<br>
Inside the .bat file, the crucial code is to have<br>
`C:\Python27\python.exe %1`

Essentially, you are making a batch file, which will call `python.exe`<br>
It will receive a parameter, in `%1`, which is the path to the `.py` file

You can add other miscellaneous like `@echo off` or `color 0f`<br>
At the end of the `.bat` file, add a `pause`<br>
This is important to prevent the console from closing<br>
And hence, allowing you to see the error logs or output

For example, my `python.bat` has the following lines

~~~
@echo off
color 0f

C:\Python27\python.exe %1

pause
~~~

With that done, let's go back to Notepad++<br>
Notepad++ has a menu which allows you to add programs to run<br>
You can show it with the F5 key

<img class="img" src="https://lh4.googleusercontent.com/-saoJfHDsGiU/UeqpLj_ilFI/AAAAAAAABBI/lTmQzd7DjJE/s1600/Untitled.png">

Specify the path to your `python.bat`<br>
And append `"$(FULL_CURRENT_PATH)"` at the end<br>
So you should have the line as below, depending on your setup<br>
`C:\Python27\python.bat "$(FULL_CURRENT_PATH)"`

Give the shortcut a name, and specify a command<br>
I personally used CTRL+ALT+P, but you're free to specify yours<br>
Just make sure it does not clash with other shortcuts in Notepad++

Once you're done, open your `.py` file and hit the shortcut command<br>
A console should appear, and execute your `.py` file<br>
It will then pause, so you could see your output

Hope this helps 