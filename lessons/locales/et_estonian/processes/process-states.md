# Protsesside olekud

## Tunni sisu

Vaatame uuesti *ps aux* käsku:

<pre>$ ps aux</pre>

STAT tulbas võib näha palju väärtusi. Linuxi protsess võib olla üsna paljudes erinevates olekutes.

<ul>
<li>R: *running* ehk *töötav*, ootab, et protsessor temaga tegeleks</li>
<li>D: *uninterruptible sleep* ehk siis protsess on *katkematus unes* - ootab, et mingi sündmus oma tööga valmis saaks, näiteks terminali sisend</li>
<li>Z: *zombi*, eelmises peatükis räägiti, et *zombid* on *töö lõpetanud protsessid*, mis ootavad, et nende oleku kohta info ära korjataks</li>
<li>T: peatunud, protsess on ajutiselt peatatud</li>
</ul>

## Harjutus

Tutvuda süsteemis töötavate protsesside ja nende olekutega.

## Küsimus

Millise STAT koodiga on esindatud segamatus unes protsessid?

## Vastus

D
