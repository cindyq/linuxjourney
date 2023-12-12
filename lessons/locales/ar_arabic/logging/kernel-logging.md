# Kernel Logging

## Lesson Content

<b>/var/log/dmesg</b>
On boot-time your system logs information about the kernel ring buffer. This shows us information about hardware drivers, kernel information and status during bootup and more. This log file can be found at /var/log/dmesg and gets reset on every boot, you may not actually see any use in it now, but if you were to ever have issues with something during bootup or a hardware issue, dmesg is the best place to look. You can also view this log using the dmesg command. 

<b>/var/log/kern.log</b>
Another log you can use to view kernel information is the /var/log/kern.log file, this logs the kernel information and events on your system, it also logs dmesg output.

## Exercise

Look at your dmesg and kern logs, what differences do you notice?

## Quiz Question

What command can be used to view kernel bootup messages?

## Quiz Answer

dmesg