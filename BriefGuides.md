# Introduction #

Here are some brief guides.


# Details #


## Deploy the requires ##

To debug your script, first of all you have to deploy the require files. If you are interpreting your scripts with a standard standalone Lua interpreter, just extract the files in the _Requires.zip_ package into the folder where the interpreter is, so that the interpretor can find them when they are required by the rld.

## Install .net Framework ##

The rld is developped under the .net platform so you need to have the .net Framework 2.0 installed. Download from Microsoft here:
http://www.microsoft.com/downloads/details.aspx?FamilyID=0856EACB-4362-4B0D-8EDD-AAB15C5E04F5&displaylang=en

## Including rld client ##

The rld client must be included in your script to debug. Simply type a
```
require"rld"
```
at the top of your script file, so this file and all the files loaded by it (using `dofile()` or `loadfile()` etc.) will be under control of rld.
A statement to launch rld should be followed:
```
rld.start()     -- Launch rld
```
After that, you can type
```
rld.bp()
```
anywhere you need a breakpoint.

## Launch the host ##

Now launch the host by double-clicking on _Remote Lua Debuuger.exe_ located in the _Debugger.zip_. Click **Host** on the toolbar on the top so it will listen to the specified port (you won't need to modify it at most cases), all the breakpoints from the corresponding client will be captured.
Once rld client a breakpoint is hit, the host will flash at the taskbar, and now you can debug your scripts with the host.

## Lite Mode ##

If you start the rld client like this:
```
rld.start(true)
```
it will turn rld into lite mode. In the lite mode, only the breakpoints made by inserting
```
rld.bp()
```
in the scripts will be processed (which means the breakpoints you set in the host will be ignored). The lite mode disables some advanced features such as conditional breakpoint, however it is real fast. If your script is performace-costing, try this mode.