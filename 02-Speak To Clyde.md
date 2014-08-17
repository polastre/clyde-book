# Speak to Clyde

Now that you've uploaded the `ClydeOriginal` application, let's speak to Clyde.

Clyde can be controlled using the USB port (a virtual serial port).  This section will familiarize yourself with Clyde's basic functions, such as the ambient eye light and the lamp.

## Get Started

Communicating with Clyde requires your first line of code.

1. In your `ClydeOriginal` application, find the line that starts with: `Serial.begin(9600);`

1. After this line, on a new line, enter:

  ```C
  while (!Serial) ;
  ```

1. Save your modified `ClydeOriginal` application.  Arduino will ask you to enter a new name for this application. Call it something catchy.

1. To send this new code to Clyde, click the **Upload** button.

1. After the upload has completed, open up the Serial Monitor.  This is in `Tools > Serial Monitor` or you can press SHIFT-COMMAND-M on Mac.

1. Next to **9600 Baud**, change the dropdown from **No line ending** to **Both NL & CR**.

## Version

Check that Clyde is working by asking him his version.

Type `VERSION` and click **Send**

You should see:

```
OK 1
```

Where **1** is your version number.

## Change lamp brightness

Send `SET_WHITE 50` to Clyde.  He'll respond with `OK`.

The number after `SET_WHITE` can be any number from 0 to 255, where 0 is off and 255 is the brighest.  Ow, 255 will hurt your eyes!

## Change the ambient eye color

SEND `SET_AMBIENT 100 150 200` to Clyde.  He'll respond with `OK`.

The number after `SET_AMBIENT` is an RGB deciminal color value (they must be integers!). Thus we just set the color to `RGB(100,150,200)`.

## Troubleshooting

If Clyde is not talking to you reliably over the serial port, make sure that `ClydeOriginal` is correctly configured to wait for the serial port to start up.  The line after `Serial.begin(9600);` should say:

```C
while (!Serial) ;
```

If it doesn't, add that line into your sketch, and re-upload the application.

**Note:** If you include `while (!Serial) ;` in your application, Clyde will not start doing anything until you open the Serial Monitor.  Be sure to remove this line when you want to remove Clyde from your PC and use him just with the power adapter.
