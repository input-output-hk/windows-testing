# windows-testing
How to set up your environment to run tests for Windows 10 machines.

We recommend installing a prebuilt Virtual Machine on your local machine.  These are provided by Microsoft.

https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/

Note that these VMs have 90 day limits, so it is sensible not to over-customise them!  We recommend using VirtualBox, which is free, and available for Windows, MacOSX, Linux and other platforms.

https://www.virtualbox.org

Just install VirtualBox, open the Windows 10 VM file that you have downloaded from Microsoft and after a while (about 10 minutes on my laptop) your Windows VM should be ready to use.  You will probably want to "Insert the Guest Additions CD" so that you can integrate the VM better with your host machine (the actual desktop/laptop etc.).  If you can't automatically open the VM file, "Add Appliance" does the same thing.  The Microsoft VM comes preinstalled with one user (IEUser), with a standard password Passw0rd!

Once you have downloaded, type command into the search box, open up the
command prompt, and type slmgr/ato to activate the system for 90 days.
You will see a response that activation has been successful.

You can then download the Windows version of Daedalus from

https://daedaluswallet.io/#download

and test and run it as a normal Windows user.


You can also download an official Windows 10 ISO image for testing purposes and create your own Virtual Machine.  There is no need to activate it - the system will just nag you occasionally.  This will not time out, but it does take more effort to set up, so is only recommended if you are familiar with using VirtualBox.  This does give more choice about the version of Windows 10 (Pro, Pro N etc.), allows you to set up your own user names, and doesn't seem to



You can provision GHC and other tools using the following Powershell script.

https://github.com/input-output-hk/ouroboros-network/blob/master/scripts/install.ps1


If you are a bash user, you may find it useful to install the Windows Subsytem for Linux (WSL).  Type "install windows subsystem for linux" into the search box and follow the instructions.
