# DNS Components

## Lesson Content

The DNS database of the Internet relies on sites and organizations providing part of that database. To do that, they need:

<b>Name Server</b>

We setup DNS via "name servers", the name servers load up our DNS settings and configs and answers any questions from clients or other servers that want to know things like "Who is google.com?". If the name server doesn't know the answer to that query, it will redirect the request to other name servers. Name servers can be "authoritative", meaning they hold the actual DNS records that you're looking for, or "recursive" meaning they would ask other servers and those servers would ask other servers until they found an authoritative server that contained the DNS records. Recursive servers can also have the information we want cached instead of reaching an authoritative server.

<b>Zone File</b>

Inside a name server lives something called zone files. Zone files are how the name server stores information about the domain or how to get to the domain if it doesn't know. 

<b>Resource Records</b>

A zone file is comprised of entries of resource records. Each line is a record and contains information about hosts, nameservers, other resources, etc. The fields consist of the following: 

<ul>
<li>Record name</li>
<li>TTL - The time after which we discard the record and obtain a new one, in DNS TTL is denoted by time, so records could have a TTL of one hour. The reason we do this is because the Internet is constantly changing, one minute a host can be mapped to X IP address then next it can be at Y IP address</li>
<li>Class - Namespace of the record information, most commonly IN is used for Internet</li>
<li>Type - Type of information stored in the record data. We won't get into record types, but you've probably seen common ones like A for address, MX or mail exchanger, etc.</li>
<li>Data - This field can contain an IP address if it's an A record or something else depending on the record type.</li>
</ul>
<pre>
patty    IN  A      192.168.0.4 
</pre>

## Exercise

No exercises for this lesson.

## Quiz Question

What resource record type is used for mail exchangers?

## Quiz Answer

MX