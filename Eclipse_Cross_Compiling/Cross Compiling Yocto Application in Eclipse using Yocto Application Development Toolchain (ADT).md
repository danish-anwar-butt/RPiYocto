# Cross Compiling Yocto Application in Eclipse using Yocto Application Development Toolchain (ADT)

1. Download Eclipse Luna with C/C++

2. Install Yocto ADT plug-in in Eclipse IDE [Details to be added...]

3. Install Yocto populated SDK into **/opt/** directory.

4. Run Eclipse IDE

5. Go to *Windows > Preferences* and open Yocto Project ADT

6. Set fields as shown below:

   ![YoctoADTPreferences](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/YoctoADTPreferences.png)

7. Create new C project

   ![CProject](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/CProject.png)

​		Click finish to complete project completion.

8. Go to *Windows > Show View*  and search for **Remote System Explorer**

9. Click on *Remote System Explorer* Tab and Click on *Define a new connection to remote* button. Following pop up windows will be shown:

   ![RSE1](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/RSE1.png)	 

10. Select **TCF** and click *next*

11. Set the **Host Name** the IP address of Raspberry Pi and **Connection Name** / **Description** appropriate name of the connection name and description of the connection.

    ![RSE2](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/RSE2.png)

12. Click on *Finish* to close the windows with default menu.

13. Right Click on **RPi3eth** in *Remote System Explorer* pane and click on *connect*

14. Enter **user id**  and **password** same on your remote target i.e. Raspberry Pi in the pop up windows as shown below and click *OK*:

    ![RSE3](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/RSE3.png)

15. If connection is successful then a green arrow will be shown on sub tabs of **RPi3eth** in *Remote System Explorer* pane

    ![RSE5](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/RSE5.png)

16. Right Click on Terminals and click connect and run some commands this will execute directly on RPi

17. Right click on **Test** in *Project Explorer* pane and select *Test_gdb_aarch64-poky-linux*

![](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/DebConf1.png)

18. Go to *Debugger* Tab and copy *GDB Debugger* field in this case `/opt/poky/3.1.20/sysroots/x86_64-pokysdk-linux/usr/bin/aarch64-poky-linux/aarch64-poky-linux-gdb`![GDBDebuggerPath](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/GDBDebuggerPath.png)

19. Goto *main* tab and Click on *Select other...* and select  as shown below and click ok

![](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/DebgConf2.png)

20. Go to *Debugger* Tab again and paste *GDB Debugger* field that was copy earlier in this case `/opt/poky/3.1.20/sysroots/x86_64-pokysdk-linux/usr/bin/aarch64-poky-linux/aarch64-poky-linux-gdb`

![DebConf3](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/DebConf3.png)

20. Goto *main* tab, select connection as RPI3eth set the target application path with respect to target machine

    ![DebConf5](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/DebConf5.png)

21. Click on **Debug** and click on *step over* button to run instructions

22. click on *stop* button to stop the application

    ![DebugWin](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/DebugWin.png)

23. click on *C/C++* button to switch to C/C++ development perspective.

24. Optionally you can verify the remote application on target and run manually there.

    ![AppMaullyRun](/media/dani/LnxData/Embedded_Linux/Build_Tools/Yocto/AppMaullyRun.png)

    

