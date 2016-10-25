# Vahendid kasutajate haldamiseks

## Tunni sisu

Paljud ärikeskkonnad kasuvad kasutajate, kontode ja salasõnade haldamiseks haldamise sütsteeme. Üksikul masinal aga saab kasutajate haldamisega hakkama kui mõne kasuliku käskudega.

<b>Kasutajate lisamine</b>

Võib kasutada *adduser* või *useadd* käske. *adduser* hõlmab aga rohkem kasulike omadusi, näiteks kodukataloogi loomine. Uute kasutajate loomiseks saab muuta seadistusfaile, sõlitvalt sellest, mida soovitakse määrata vaikimisi kasutajale.

<pre>$ sudo useradd peeter</pre>

Viimane käsk loob peetri kohta sisestuse faili /etc/passwd, loob vaikimis grupi ka lisab sisestuse ka faili /etc/shadow.

<b>Kasutajate kustutamine</b>

Kasutaja kustutamiseks võib kasutada *userdel* käsku.

<pre>$ sudo userdel peeter</pre>

Põhimõtteliselt annab see käsk endast parima, et võtta tagasi muudatused mida *useradd* failidesse tegi.

<b>Salasõna muutmine</b>

<pre>$ passwd peeter</pre>

Selle käsuga saab muuta enda või mõne teise kasutaja prooli (muidugi juhul kui oled juurkasutaja).

## Harjutus

Luua uus kasutaja, muuta tema parool ja siis selle kasutajana sisse logida.

## Küsimus

Millise käsuga saab muuta kasutajate paroole?

## Vastus

passwd
