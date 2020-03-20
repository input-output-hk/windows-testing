# How to set up your machine for Windows 10 testing if you are not running Windows 10 natively
How to set up a Virtual Machine environment to run Daedalus or perform tests for Windows 10 environments.

## Advice on Running Windows 7 or 8
Don't.

## Set up a Pre-built Virtual Machine to run Windows 10 on your Mac, Linux or other system

We recommend installing a pre-built Virtual Machine on your local machine.  These are provided by Microsoft.

https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/

Note that these VMs have 90 day limits, so it is sensible not to over-customise them!  We recommend using `VirtualBox`, which is free, and available for Windows, MacOSX, Linux and other platforms.

https://www.virtualbox.org

Just install `VirtualBox`, open the Windows 10 VM file that you have downloaded from Microsoft and after a while (about 10 minutes on my laptop) your Windows VM should be ready to use.  You will probably want to "Insert the Guest Additions CD" so that you can integrate the VM better with your host machine (the actual desktop/laptop etc.).  If you can't automatically open the VM file, "Add Appliance" does the same thing.  The Microsoft VM comes preinstalled with one user (IEUser), with a standard password `Passw0rd!`

Once you have downloaded the files, start the Virtual Machine and log in.

Type `command` into the Windows 10 search box, open up the
`command prompt` application, and type `slmgr/ato` to activate the system for 90 days.
You will see a response that activation has been successful.

You can then download the Windows version of `Daedalus` from

https://daedaluswallet.io/#download

using the Microsoft Edge browser, and then install, test and run it as a normal Windows user.  Take care to keep up to date with all security updates, and be careful about giving the VM access to your host file system.  You are running a live Windows machine that is connected to the Internet!

## Set up your own Virtual Machine running Windows 10

If you prefer, you can instead download an official Windows 10 ISO image for testing purposes and create your own Virtual Machine.  There is no need to activate Windows in this case - the system will just nag you occasionally.  The installation will not time out, but it does take more effort to set up, so is only recommended if you are familiar with using VirtualBox.  This does give more choice about the Windows 10 edition (Pro, Pro N etc.), allows you to set up your own user names, and doesn't seem to be as restricted as the official Windows VM, so you may find it more useful if you are a developer.

https://www.microsoft.com/en-gb/software-download/windows10ISO


## Instructions for those needing to Run GHC etc (Developers/Testers)


You can provision GHC and other tools using the following Powershell script.

https://github.com/input-output-hk/ouroboros-network/blob/master/scripts/install.ps1

Github don't make downloads easy.  You may want to install Github Desktop to be able to download and run this script.  Once downloaded, right-click on it and run it in Powershell.  You do want to change the Execution Policy to allow this.
This will install chocolatey and then Cabal and GHC.  You can run cabal/ghc from the Command Prompt.

There is a guide here on how to install GHC using chocolately.

https://hub.zhox.com/posts/introducing-haskell-dev/ by Tamar (who maintains the chocolatey ghc package).
hub.zhox.comhub.zhox.com


If you are a bash user, you may find it useful to install the Windows Subsytem for Linux (WSL).  Type "install windows subsystem for linux" into the search box and follow the instructions.  I haven't yet figured out how to do this with the Microsoft pre-configured VM.  I think you probably need to download some other things first...
