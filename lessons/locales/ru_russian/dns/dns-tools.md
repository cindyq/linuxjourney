# Инструменты DNS

## Содержание урока

<b>nslookup</b>

Средство поиска имени сервера используется для запроса серверов имен для поиска информации о записях ресурсов. Давайте найдем, где сервер имен для google.com:

<pre>
pete@icebox:~$ nslookup www.google.com
Server:         127.0.1.1
Address:        127.0.1.1#53

Non-authoritative answer:
Name:   www.google.com
Address: 216.58.192.4
</pre>

<b>dig</b>

Dig (domain information groper) - это мощный инструмент для получения информации о DNS-серверах имен, он более гибок, чем nslookup, и отлично подходит для решения проблем DNS.


<pre>
pete@icebox:~$ dig www.google.com

; <<>> DiG 9.9.5-3-Ubuntu <<>> www.google.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 42376
;; flags: qr rd ra; QUERY: 1, ANSWER: 5, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; MBZ: 0005 , udp: 512
;; QUESTION SECTION:
;www.google.com.                        IN      A

;; ANSWER SECTION:
www.google.com.         5       IN      A       74.125.239.147
www.google.com.         5       IN      A       74.125.239.144
www.google.com.         5       IN      A       74.125.239.146
www.google.com.         5       IN      A       74.125.239.145
www.google.com.         5       IN      A       74.125.239.148

;; Query time: 27 msec
;; SERVER: 127.0.1.1#53(127.0.1.1)
;; WHEN: Sun Feb 07 10:14:00 PST 2016
;; MSG SIZE  rcvd: 123
</pre>

## Задание

Прочитайте спровочную страницу для dig

## Вопрос

Какой инструмент используется для получения подробной информации о DNS-серверах имен?

## Ответ

dig