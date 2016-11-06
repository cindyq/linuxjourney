# Lähtekoodi kompileerimine

## Tunni sisu

Vahel võib sattuda mõne sellise segase paketi otsa, mis on saadaval ainult puhtas lähtekoodis. Selleks, et seda kompileerida ja paigaldada on vaja teada paari käsku.

Esiteks on aga vaja tarkvara, et paigaldada tööriistad, mis võimaldaksid lähtekoodi kompileerida.

<pre>$ sudo apt install build-essential</pre>

Kui see on tehtud, on vaja paketi faili sisu lahti pakkida. See on ilmselt .tar.gz fail.

<pre>$ tar -xzvf pakett.tar.gz</pre>

Enne kui üldse midagi tegema hakata, võiks lugeda *README* või *INSTALL* faili paketis. Mõnikord võib sealt leida paigaldamiseks spetsiifilisi juhiseid. 

Olenevalt sellest, milliseid kompileerimise meetodeid kasutas arendaja, võib vaja minna erinevaid käske, näiteks *cmake* või midagi muud.

Tavalisemalt kasutatakse aga ikkagi *make* kompilatsiooni, seega räägitakse just sellest lähemalt:

Paketis asub konfiguratsiooni skript, mis kontrollib süsteemis sõltuvusi. Kui midagi on puudu, antakse veateade ning vajalikud asjad tuleb ära parandada.

<pre>$ ./configure</pre>

<b>./</b> võimaldab käivitada skripti jooksvast kataloogist.

<pre>$ make</pre>

Paketis asub ka fail nimega Makefile, mis sisalfab reegleid tarkvara ehitamiseks. Kui sisestada *make* käsk, vaadatakse just selle faili sisse.

<pre>$ sudo make install</pre>

See käsk paigaldab paketi, õige fail kopeeritakse arvutis õigesse kohta.

<pre>$ sudo make uninstall</pre>

*make install* käsku kasutades tasuks olla ettevaatlik, võib olla üllatav kui palju tegelikult tasutal toimub. Kui hakata seda paketti hiljem eemaldama, ei pruugi kõik oluline eemaldatud saada, kuna kasutaja ei ole tadlik kui palju täpselt midagi süsteemi lisati. Kui nüüd järgi mõelda, siis ehk tasuks kogu jutt *make install*i kohta ära unustada ja kasutada hoopis käsku  <b>*checkinstall*</b>. Nõnda luuakse .deb fail, mida on kerge paigaldada ja eemaldada.

<pre>$ sudo checkinstall</pre> 

Selle käsuga sisuliselt *make install*itakse ja ehitatakse .deb pakett ning ka paigaldatakse see. See teeb hiljem eemaldamise lihtsamaks.

## Harjutus

Leida usaldusväärselt veebilehelt lähtekoodiga programm ning paigaldada see allikast.

## Küsimus

Mida peaks ALATI kasutama *make install* asemel?

## Vastus

checkinstall

