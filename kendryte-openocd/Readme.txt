/-------------------------------------\
|    Kendryte OpenOCD Win32 Binary    |
|           version: 0.2.3            |
|          data: 2018/02/21           |
\-------------------------------------/

===============================================================================
                                  Requirement
===============================================================================

First, Run `zadig-2.4.exe` in `tool/`, `Options` -> `List all devices`, select
your JTAG simulator and convert the vendor drivers to WinUSB drivers.

===============================================================================
                                  Quickstart
===============================================================================

We have provided a template configuration for J-Link in `tcl/kendryte.cfg`,
if you are using other JTAG simulators, please modify it yourself.

We added a command line argument '-m', it can set the debug mode, now you have
two options, `-m0` for debugging core 0 while `-m1` for debugging core 1, and 
the `-m0` is the default option.

You can start the openocd simply by using the following command:
  
  ./bin/openocd -f ./tcl/kendryte.cfg -m0

After OpenOCD startup, connect GDB with

  (gdb) target remote :3333

then start your debugging! :)

More information: https://github.com/kendryte/openocd-kendryte/wiki

===============================================================================
                                  Bug report
===============================================================================

If you have some problems, you can open a issue at

  https://github.com/kendryte/openocd-kendryte/issues
   
Thank you for your use.