# Getting Ready to Program Clyde

By now you've received your Clyde and you've played with its basic functionality.

Here's how you get started programming it.

## Preparing your computer

1. [Download Arduino software](http://arduino.cc/en/Main/Software).
1. [Download Clyde libraries as a zip file](https://github.com/fabule/Clyde/archive/master.zip).
1. Open the zip file.
1. Copy all of the folders in `software/arduino/libraries` to your `arduino/libraries` directory (usually in your home directory on your PC).  If the `arduino/libraries` folder doesn't exist, create it.  You'll need to copy **Clyde**, **SerialCommand**, and **MPR121**.
1. [Download kroimon's SerialCommand](https://github.com/kroimon/Arduino-SerialCommand/archive/master.zip).
1. Delete the existing `arduino/libraries/SerialCommand` and replace it with the unzipped folder from kroimon's SerialCommand.
1. Copy `software/arduino/hardware/1.0.5` to your `ardunio/hardware` directory.
1. Open up the Arduino application.
1. Under `Tools > Board`, select **Clyde**.
1. Open `File > Examples > Clyde > Examples > ClydeOriginal`.

## Preparing Clyde

1. Plug Clyde in.  Yes, I know this sounds weird because you'll be connecting Clyde to your computer, but the USB simply isn't powerful enough to make Clyde work.  Don't worry, the power supply is isolated.
1. Plug USB in.
1. Test the Clyde is still doing his factory default behavior by pressing the eye a few times.
1. Set your serial port under `Tools > Serial Port` to match the USB device that appeared when you plugged Clyde in.  When in doubt, select the last `tty` option.

## Program Clyde for the First Time

1. Press the **Upload** button, second from the top left to upload code to Clyde.
1. When it says "Done uploading.", Clyde will flash once.
1. Test that you can still turn on/off Clyde's eye and light by pressing the eye.

**Congratulations!** You've uploaded your first Clyde application.  Let's get on to building applications for Clyde.

## Troubleshooting

If Clyde doesn't do anything when pressing the eye, make sure that both the power and USB cords are connected to Clyde.

If there's an error compiling `ClydeOriginal`, it may be because you haven't copied over all _three_ libraries.  Remember that after you add or delete Arduino libraries, you need to restart the Arduino application
