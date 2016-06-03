# env (Environment)

## Lesson Content

Run the following command: 

<pre>$ echo $HOME</pre>

You should see the path to your home directory, mine looks like /home/pete. 

What about this command? 

<pre>$ echo $USER </pre>

You should see your username!

Where is this information coming from? It's coming from your environment variables:

<pre>$ env </pre>

This outputs a whole lot of information about the environment variables you have. These variables contain useful information that the shell uses in scripts and other processes they are denoted with a $ at the beginning of the variable name.

One particularly important variable is $PATH. 

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin</pre>

This returns a list of paths separated by a colon that your system searches for when it runs a command. Let's say you download a binary from the internet and put it in your ~/Downloads folder and want to run that command, you type $ coolcommand and the prompt says command not found. Well that's silly you are looking at the binary in the Downloads folder and know it exists. What is happening is that $PATH variable doesn't check the ~/Downloads folder for this binary so it's throwing an error. 

Let's say you had tons of binaries you wanted to run out of your ~/Downloads folder, you can just modify the PATH variable to include those paths. 

## Exercise

What does the following output? Why?
<pre>$ echo $hOmE</pre>

## Quiz Question

How do you see your environment variables?

## Quiz Answer

env