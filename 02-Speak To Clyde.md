# Speak to Clyde

Now that you've uploaded the `ClydeOriginal` application, let's speak to Clyde.

Clyde can be controlled using the USB port (a virtual serial port).

## Get Started

Start communicating with 2 easy steps.

1. Open up the Serial Monitor.  This is in `Tools > Serial Monitor` or you can press SHIFT-COMMAND-M on Mac.
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

## Troubleshooting

If Clyde is not talking to you reliably over the serial port, make sure that `ClydeOriginal` is correctly configured to wait for the serial port to start up.  The line after `Serial.begin(9600)` should say:
```
while (!Serial) ;
```
If it doesn't, add that line into your sketch, and re-upload the application.