# DNS Setup

## Lesson Content

We won't got through setting up a DNS server, as that would be quite a lengthy tutorial. Instead here is a quick comparison list of the popular DNS servers to use with Linux.

<b>BIND</b>

The most popular DNS server on the Internet, it's the standard that is used with Linux distributions. It was originally developed at the University of California at Berkeley hence the name BIND (Berkeley Internet Name Domain). If you need full-featured power and flexibility, you can't go wrong with BIND.

<b>DNSmasq</b>

Lightweight and much easier to configure than BIND. If you want simplicity and don't need all the bells and whistles of BIND, use DNSmasq. It comes with all the tools you need to setup DHCP and DNS, recommended for a smaller network.

<b>PowerDNS</b>

Full-featured and similar to BIND, it offers you a little bit more flexibility with options. It reads information from multiple databases such as MySQL, PostgreSQL, etc. for easier administration. Just because BIND has been the way we do things, it doesn't mean it has to stay that way.

This isn't a complete list, but it should give you an idea of where to look if you are setting up your own DNS server. 

## Exercise

No exercises for this lesson.

## Quiz Question

What is the de facto DNS server for Linux?

## Quiz Answer

BIND