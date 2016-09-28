# pwd (Print Working Directory)

## Tunni sisu

Linuxis on kõik asjad failid. Mida sügavamale Linuxi maailma sa rändad, seda paremini hakkad sa seda mõistma. Hetkel pea see aga lihtsalt meeles. Kõik failid on organiseeritud hierarhilise kataloogipuuna. Failisüsteemi esimese kataloogi nimi on väga asjakohaselt juurkataloog. Juur kataloogis asub palju kaustu ja faile, milles omakorda asub veel kaustu ja faile jne. Näide, kuidas kataloogi puu võib välja näha:

<pre>/
|-- bin
|   |-- file1
|   |-- file2
|-- etc
|   |-- file3
|   `-- directory1
|       |-- file4
|       `-- file5
|-- home
|-- var
</pre>

Failide ja Kataloogide puhul räägitakse nende asukohast. Kui sul oleks kaust nimega home, mille sees oleks pete nimeline kaust, mille sees omakorda oleks kaust Filmid, siis näeks selle asukoht välja järgmine: /home/pete/Filmid. Lihtne, või mis?

Failisüsteemis, nagu ka reaalses maailmas, teeb navigeerumise oluliselt lihtsamaks, kui sa tead, kus sa asud ja kuhu sa minna tahad. Selleks, et näha, kus sa asud, võid kasutada käsku pwd. Tõlkes tähendab see käsk "kuva jooksev kataloog" ning see lihtsalt näitabki sulle, millises kataloogis sa asud. Pane tähele, et asukoht algab juurkataloogist.


<pre>$ pwd</pre>

Kus sa oled? Kus mina olen? Proovi järgi.

## Harjutus

Selles peatükis harjust ei ole.

## Küsimus

Kuidas sa saad teada, millises kataloogis sa parasjagu oled?

##

pwd