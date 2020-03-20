# windows-testing
How to set up your environment to run tests for Windows 10 machines.

We recommend installing a prebuilt Virtual Machine on your local machine.  These are provided by Microsoft.

https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/

Note that these VMs have 90 day limits, so it is sensible not to over-customise them!  We recommend using VirtualBox, which is free, and available for Windows, MacOSX, Linux and other platforms.

https://www.virtualbox.org

Just install it, click on Import Appliance and after a while your Windows VM should be ready to use.

You can also download an official Windows 10 ISO for testing purposes and create your own Virtual Machine.  There is no need to register it - the system will just nag you occasionally.  This will not time out, but it does take more effort to set up, so is only recommended if you are familiar with using VirtualBox.


You can provision GHC and other tools using the following script.

https://github.com/input-output-hk/ouroboros-network/blob/master/scripts/install.ps1
