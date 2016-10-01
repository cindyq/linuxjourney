# sort

## Tunni sisu

Sort käsk on kasulik ridade sorteerimiseks.

<pre>
fail1.txt
koer
lehm
kass
elevant
lind

$ sort fail1.txt
elevenat
kass
koer
lehm
lind
</pre>

Saab teha ka tagurpidise sorteerimise:

<pre>$ sort -r fail1.txt
lind
lehm
koer
kass
elevant
</pre>

Samuti ka numbrilise väärtuse põhjal:

<pre>$ sort -n fail1.txt
--pean järgi proovima--
</pre>

## Harjutus

Sort käsu tõeline jõud tuleneb võimalusest kasutada seda koos teiste käskudega. Proovi järgmist käsku ja vaata, mis juhtub?

<pre>$ ls /etc | sort -rn</pre>

## Küsimus

Millise käsuga saab teha tagurpidi soreteerimist?

## Vastus

-r
