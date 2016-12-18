# Mälu seire

## Tunni sisu

Lisaks protsessori ja sisendi/väljundi seirele saab teostada ka mälu kasutuse seiret, seda käsuga <b>vmstat</b>.

<pre>
pete@icebox:~$ vmstat
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 1  0      0 396528  38816 384036    0    0     4     2   38   79  0  0 99  0  0
</pre>

Väljas on järgmised:

<b>procs</b>
<ul>
<li>r - protsesside arv töötamise jooksul</li>
<li>b - protsesside arv katkematus unes</li>
</ul>

<b>memory</b>
<ul>
<li>swpd - virtuaalmälu kasutamise kogus</li>
<li>free - vaba mälu kogus</li>
<li>buff - puhvrina kasutatava mälu kogus</li>
<li>cache - vahemäluna kasutatava mälu kogus</li>
</ul>

<b>swap</b>
<ul>
<li>si - sisse saalitud mälu kogus</li>
<li>so - välja saalitud mälu kogus</li>
</ul>

<b>io</b>
<ul>
<li>bi - plokkseadmelt vastu võetud plokkide kogus</li>
<li>bo - plokkseadmele saadetud plokkide kogus</li>
</ul>

<b>system</b>
<ul>
<li>in - katkestuste kogus sekundi kohta</li>
<li>cs - kontekstkommutatsioonide kogus sekundi kohta</li>
</ul>

<b>cpu</b>
<ul>
<li>us - kasutaja ajas veedetud aeg</li>
<li>sy - tuuma ajas veedetud aeg</li>
<li>id - Kasutamata veedetud aeg</li>
<li>wa - sisendi/väljundi järgi ootamise aeg</li>
</ul>

## Harjutus

Uurida mälukasutust vmstat'iga.

## Küsimus

Millise tööriistaga kuvatakse mälu kasutust puudutav info?

## Vastus

vmstat
