# About

*Cocoduino* is an IDE for the Arduino platform written in native Cocoa. It's designed to be simple and easy to use and is a replacement for the official Arduino IDE.

Cocoduino plays perfectly well together with the official Arduino IDE without any compatibility problems.

![Cocoduino](http://fabian-kreiser.com/cocoduino/cocoduino-screenshot.png)

# Download

You can download the latest version of the application [here](http://fabian-kreiser.com/cocoduino/cocoduino.zip).

Make sure you have the [official Arduino IDE](http://arduino.cc/en/Main/Software) installed, because Cocoduino relies on tools that are shipped with it.

### System Requirements:

* **Mac OS X 10.7 Lion** *(64 Bit)*

# Features

Cocoduino offers nearly the same features as the official Arduino IDE:

* **Sketchbook**
* **Serial Monitor**
* **Integrated Examples**
* **Multiple Files or Tabs**
* **Build and Upload to your Arduino**

Additionally, it supports Mac OS X features like:

* **Autosave**
* **Versions**
* **Fullscreen**

Last but not least, there is also:

* **Syntax Coloring**
* **Basic Code Completion**

# Limitations

1. **Build Process**
    
    As there is no official `CLI` interface for the Arduino build process, there is no guarantee that Cocoduino can compile all sketches that work with the official Arduino IDE.  
*There might be problems with more complex sketches.*

2. **File Architecture**
    
    The official Arduino IDE uses plain text files for sketches with a path extension of `.ino`. Those sketches need to be located inside a directory with the same name as the main sketch file's name.  
    When using `NSDocument`, you'd actually want to use a binary data file which is far more powerful, because you can store additional metadata within the file. Or store multiple files in a single one, etc.  
    In order to preserve full compatibility to the official Arduino IDE, Cocoduino uses some hacks in order to support the same file architecture as the official Arduino IDE. There are some disadvantages when doing this: *Autosave* doesn't work without additional work and *Versions* is buggy. All in all, I think this was the right decision.

3. **Upload using Programmers**

    While Cocoduino supports nearly all Arduino boards *theoretically*, the use of *programmers* is neither tested nor "officially supported".

# On the List…

* **Clean up the syntax coloring library**
* **More advanced code completion** (Cocoduino is ignoring the *keywords.txt* files!)

# F.A.Q

1. **Will you add…?**

    Only if I think it'd improve the application. You are free to fork the project, though. (That's why it's open source.)

2. **My sketch won't compile**

    If you have problems with one particular sketch, please post to the [issues](https://github.com/fabiankr/Cocoduino/issues).

3. **Application crashes**

    *To err is human*. Please post the crash log to the [issues](https://github.com/fabiankr/Cocoduino/issues).

# Acknowledgments

Cocoduino uses *(modified)* versions of the following third party libraries:

* [Sparkle](http://sparkle.andymatuschak.org/)
* [SCEvents](http://stuconnolly.com/projects/code/)
* [AMSerialPort](http://www.harmless.de/cocoa-code.php)
* [MASPreferences](https://github.com/shpakovski/MASPreferences)
* [PSMTabBarControl](http://www.positivespinmedia.com/dev/PSMTabBarControl.html)
* [Fragaria](https://github.com/mugginsoft/Fragaria)

The tool used for the actual build process is *(modified and with additional preprocessing)*:

* [Ino](http://inotool.org/)

# License
MIT License

	Copyright (c) 2013 Fabian Kreiser
	
	Permission is hereby granted, free of charge, to any person obtaining a copy of
	this software and associated documentation files (the "Software"), to deal in
	the Software without restriction, including without limitation the rights to use,
	copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the
	Software, and to permit persons to whom the Software is furnished to do so,
	subject to the following conditions:
	
	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.
	
	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
	FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
	COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
	IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
	CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.