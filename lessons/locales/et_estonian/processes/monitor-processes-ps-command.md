# ps (Protsessid)

## Tunni sisu

Protsessid on arvutis töötavad programmid. Neid haldab tuum ja neil kõigil on oma ID, mida nimetatakse <b>protsessi IDks (PID)</b>. Need IDd jagatakse välja protsessside loomise järjekorras.

*ps* käsku sisestades saab näha nimekirja töötavatest protsessidest:

<pre>$ ps

PID        TTY     STAT   TIME          CMD
41230    pts/4    Ss        00:00:00     bash
51224    pts/4    R+        00:00:00     ps
</pre>

Kiire ülesvõte protsesside kohta annab järgmist infot:

<ul>
<li>PID: Protsessi ID</li>
<li>TTY: Protsessiga seotud terminal (sellest pikemalt veidi hiljem)</li>
<li>STAT: Protsessi staatuse kood</li>
<li>TIME: Kumulatiivne protsessori kasutamise aeg</li>
<li>CMD: Käsu/käivitatud rakenduse nimi</li>
</ul>

*Ps*i *man* lehet võib leida palju erinevaid võimalusi selle käsu sisestamiseks. Need erinevad veidi sõltuvalt, millist variant soovitatakse kasutada - BSG, GNU või Unix. Tõenäolisel ton BSD stiil teistest natuke populaarsem, seega kasutatakse sellel kursusel seda. Uudishimu rahuldamiseks võib öelda, et erunevus seisneb selles mitut kriipsu kasutatakse ja lippudes.
 
<pre>$ ps aux</pre>

<b>a</b> kuvab kõik töötavad protsessid, kaasaaravtud need, mis töötavad teiste kasutajate all. <b>u</b> kuvab protsesside kohta rohkem detaile ja viimaks, <b>x</b> kuvab kõik protsessid, millega ei ole TTYd seostatud. Nened protsessidel on ? TTY väljas. Selline asi on väga levinud deemoni protsessides, mis seotud süsteemi käivitumisega.

Selle käsuga on näga oluliselt rohkem välju. Neid pole vaja kõiki meelde jätta, järgmises peatükkis, kus räägitakseprotsessidest lähemalt, räägitakse neist uuesti:

<ul>
<li>USER: Kehtiv kasutaja (see kelle ligipääsuõigusi kasutatakse)</li>
<li>PID: Protsessi ID</li>
<li>%CPU: Protessori aja kasutuse suhe aega, mis protsess on töötanud</li>
<li>%MEM: Ratio of the process's resident set size to the physical memory on the machine</li>
<li>VSZ: Protsessi virtuaalmälu kasutus</li>
<li>RSS: Resident set size, saalimata füüsiline mälu, mida tegum on kasutanud</li>
<li>TTY: Protessiga seostatud terminal</li>
<li>STAT: Protsessi staatuse kood</li>
<li>START: Protsessi käivitumise aeg</li>
<li>TIME: Kumulatiivne protsessori kasutamise aeg</li>
<li>COMMAND: Käsu/käivitatud rakenduse nimi</li>
</ul> 

*ps* käsu vaatamine võib muutuda tülikaks, hetkel uurime kõige rohkem välju PID, STAT ja COMMAND.

Teine väga kasulik käsk on *top*. See kuvab sulle töötavate protsesside kohta juba mitte enam hetke ülesvõtet, vaid jooksvat informatsiooni. Vaikimisi uuendatakse kuva iga 10 sekundi järel. *Top* on äärmisel kasulik vahend kui on vajalik teada, milised protsessid kasutavad suurem määral arbuti ressursse.

<pre>$ top</pre>

## Harjutus

Kasutada *top*o erinevate lippudega ja pöörata tähelepanu sellele, kuidas muutub kuvatav info.

## Küsimus

Millise lipuga kuvatakse protsesside kohta detailset infot?

## Vastus

u
