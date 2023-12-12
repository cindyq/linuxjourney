# syslog

## Lesson Content

The syslog service manages and sends logs to the system logger. Rsyslog is an advanced version of syslog, most Linux distributions should be using this new version. The output of all the logs the syslog service collects can be found at /var/log/syslog (every message except auth messages).

To find out what files are maintained by our system logger, look at the configuration files in /etc/rsyslog.d:

<pre>
pete@icebox:~$ less /etc/rsyslog.d/50-default.conf 
# First some standard log files.  Log by facility.
#
auth,authpriv.*                 /var/log/auth.log
*.*;auth,authpriv.none          -/var/log/syslog
#cron.*                         /var/log/cron.log
#daemon.*                       -/var/log/daemon.log
kern.*                          -/var/log/kern.log
#lpr.*                          -/var/log/lpr.log
mail.*                          -/var/log/mail.log
#user.*                         -/var/log/user.log
</pre>

These rules to log files are denoted by the selector on the left column and the action on the right column. The action tells us where to send the log information, in a file, console, etc. Remember not every application and service uses rsyslog to manage their logs, so if you want to know specifically what is logged you'll have to look inside this directory.

Let's actually see logging in action, you can manually send a log with the logger command:

<pre>
logger -s Hello
</pre>

Now look inside your /var/log/syslog and you should see this entry in your logs!

## Exercise

Look at your /etc/rsyslog.d configuration file and see what else is being logged via the system logger.

## Quiz Question

What command can you use to manually log a message?

## Quiz Answer

logger