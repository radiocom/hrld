# Introduction #

Introduces how to make a quick start to HRLD


# Details #

  1. Be sure you have .net Framework 2.0 installed. You can download it at http://www.microsoft.com/downloads/details.aspx?FamilyID=0856EACB-4362-4B0D-8EDD-AAB15C5E04F5&displaylang=en
  1. Extract files in _Requires.zip_ into a location which is reachable for your Lua intepretor. For example, under the folder where you have Lua 5.1 installed.
  1. In the Lua script file which you want to debug, add two lines of code:
```
require"rld"	-- will search for rld library
rld.start()	-- start rld and fire a break immediatly
```
  1. Launch Lua Remote Debugger.exe under _Debugger.zip_ and click **Host** on the toolbar to launch the host.
  1. Run your Lua script.