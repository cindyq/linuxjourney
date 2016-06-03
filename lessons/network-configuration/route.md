# route

## Lesson Content

We've already discussed viewing our routing tables with the route command, if you wanted to add or remove routes you can do so manually.

<b>Add a new route</b>

<pre>
$ sudo route add -net 192.168.2.1/23 gw 10.11.12.3
</pre>

<b>Delete a route</b>

<pre>
$ sudo route del -net 192.168.2.1/23 
</pre>

## Exercise

No exercises for this lesson.

## Quiz Question

What is the command flag to delete a route?

## Quiz Answer

del