# join and split

## Lesson Content

The join command allows you to join multiple files together by the position of their lines: 

Let's say I had two files that I wanted to join together:
<pre>file1.txt
John
Jane
Mary

file2.txt
Doe
Doe
Sue

$ join file1.txt file2.txt
John Doe
Jane Doe
Mary Sue
</pre>

See how it joined together my files? Pretty neat. You can also split a file up into different files with the split command: 

<pre>$ split somefile</pre>

This will split it into different files, by default it will split them once they reach a 1000 line limit. The files are named x** by default.

## Exercise

Join two files with different number of lines in each file, what happens?

## Quiz Question

What command would you use to join files named cat dog cow?

## Quiz Answer

join cat dog cow