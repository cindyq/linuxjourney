# Ülevaade failide jagamisest

## Tunni sisu

Tavaliselt ei ole kasutaja oma arvutiga võrgus üksi ja seda kindlasti mitte siis, kui teha tööd kommertskeskkonnas. Selleks, et kanda mingeid faile ühest arvutist teise, võib mõnikord olla lihtsam kasutada USB pulka kopeerides failid käsitsi. Kuid enamasti, kui teha tööd samas võrgus, jagatakse faile läbi võrgu.

Sellel kursusel tutvustatakse mõnda  andmete kopeerimise meetodit, mida saab rakendada samas võrgus paiknevate arvutite peal. Arutlusele tulevad mõned lihtsamad failide kopeerimise meetodid, seejärel aga, kuidas haakida terveid katalooge, et nad käituksid kui eraldiseisvad kettad.

Üks lihtne failide jagamise tööriist on  <b>scp</b> käsk. Inglise keelest tõlgituna tähendab see käsk turvalist kopeerimist (*secure copy*). See töötab just nagu cp käsk, kuid võimaldab kopeerida erinevate lõppkasutajate vahel. Kuna see töötab läbi SSH, kasutavad kõik tegevused sama autentimist ja turvalisust kui SSH.

<b>Selleks, et kopeerida fail kohalikust arvutist eemal asuvasse arvutisse</b>

<pre>$ scp minufail.txt kasutajanimi@kaugarvuti.com:/eemalasuv/kataloog</pre>

<b>Selleks, et kopeerida fail eemalasuvast arvutis enda omasse</b>

<pre>$ scp kasutajanimi@kaugarvuti.com:/eemalasuv/kataloog/minufail.txt /kohalik/kataloog</pre>

<b>Selleks, et kopeerida kataloog enda arvutist eemalasuvasse arvutisse</b>

<pre>$ scp -r minukataloog kasutajanimi@kaugarvuti.com:/eemalasuv/kataloog</pre>

## Harjutus

Proovida kopeerida faili scp abil ühest arvutist teise.

## Küsimus

Millise käsuga saab turvaliselt kopeerida faile ühest arvutist teise?

## Vastus

scp
