<h1>Help Desk Ticket: Computer Startup Troubleshooting</h1>

<h2>Description</h2>
A user had the following issue:<br>
My computer is giving me a black screen with a bunch of confusing text when I try to turn it on. I'm using my phone to send this 'cause I can't get past this screen.
If you could check it out and help me out ASAP, that'd be awesome. Got work waiting.

<h2>Troubleshooting Process</h2>

I powered up the computer and got the Windows Boot Manager with the message “The Boot Configuration Data for your PC is missing or contains errors”.

- <b>Theory 1: The boot configuration data is corrupted. I restarted the computer and booted from a Windows CD; I then chose the “Repair your Computer” option > Troubleshoot > Command Prompt from there, I ran check the disk partitions (diskpart), listed the disks (list disk), selected disk 0, listed the partitions (list partition), selected the partition where Windows was installed, marked the partition as active, and then exited. I then clicked “Continue to Windows 10”, removed the disk from the CD drive, and restarted the computer; the computer now boots up and launches Windows.</b>

<h2>Resolution</h2>

- <b> Resolution (Internal): It looks like the partition for the BCD file was not marked as “active” and the system could not located the boot files; using a Windows CD, I was able to boot the computer and get into the command prompt to check the disk partition and mark the partition where Windows was installed as “active” which then allowed me to remove the CD and reboot the computer from the hard drive
- <b> Resolution (Client-Facing): I looked through the storage on the computer, located where the files for your Windows operating system are stored, and then marked this as the part for the computer to use when starting up. Now it knows where to find the files it needs to launch Windows.

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
