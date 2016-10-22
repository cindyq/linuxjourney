# /etc/shadow

## Tunni sisu

Failis /etc/shadow hoiatakse kasutajate tuvastamist puudutavat informatsiooni. Lugemiseks on vaja juurkasutaja õigusi.

<pre>$ sudo cat /etc/shadow

root:MyEPTEa$6Nonsense:15000:0:99999:7:::
</pre>

Võib märgata, et sisu on /etc/passwd omale väga sarnane. Küll aga on parooli koha peal hoopis krüpteeritud salasõna. Koolonitega eraldatud väljad on järgmised:

<ol>
<li>Krüpteeritud salasõna</li>
<li>Viimase parooli muutmise kuupäev - väärtus on päevades alates 1. jaanuaris 1970. Kui selle koha peal on 0, peaks kasutaja järgmisel sisenemisel parooli ära muutma</li>
<li>Minimaalne parooli vanus - päevade arv, mida kasutaja peab ootama, enne kui võib salasõna muuta</li>
<li>Maximaalne parooli vanus - maksimaalne päevade arv, kuni peab parooli muutma</li>
<li>Parooli hoiatuse periood - päevade arv, mis on jäänud salasõna aegumiseni</li>
<li>Parooli passiivsuse periood - päevade arv pärast parooli aegumist kui on veel lubatud selle parooliga siseneda</li>
<li>Konto aegumise kuupäev - kuupäev, millal kasutaja ei saa enam sisenea</li>
<li>Väli, mis on reserveeritud mingil tulevasel eesmärgil</li>
</ol>

Paljudes distributsioonides ei sõltu kasutajate tuvastamine enam ainule /etc/shadow failist. Autentimist asendavad teised mehhanismid, näiteks PAM (*Pluggable Autehntication Modules*).

## Harjutus

Vaadata /etc/shadow faili sisse.

## Küsimus

Küsimust pole.

## Vastus


