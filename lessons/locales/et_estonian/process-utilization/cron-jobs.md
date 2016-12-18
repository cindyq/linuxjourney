# Croni tegumid

## Tunni sisu

Kuigi oleme rääkinud ressursside kasutusest, võiks olla hea hetk mainida toredat Linuxi tööriista, croni, mida kasutatakse tegumite ajastamiseks. On olemas teenus, mis võimaldab programmidel töötada just siis kui kasutaja on selle ajastanud. See on eriti kasulik näiteks siis, kui kasutaja tahab regulaarselt korra päevas käivitada mingit skript.

Ütleme, et on olemas skript, mille otsiteekond on /home/pete/scripts/muuda_taustapilt. Kasutaja kasutab seda igal hommikul, et muuta töölaua taustapildina kasutatavat pilti. Kuid igal hommikul peab seda skripti käsitsi käivitama. Selle asemel võiks aga luua cron'i tegumi, mis käivitab skripti läbi cron'i. Skripti käivitamise ja croni tegumi aktiveerimise aeg määratakse kasutaja poolt.

<pre>30 08 * * * /home/pete/scripts/muuda_taustapilt</pre>

Väljad vasakult paremale on järgmised:
<ul>
<li>Minut - (0-59)</li>
<li>Tund - (0-23)</li>
<li>Kuupäev - (1-31)</li>
<li>Kuu - (1-12)</li>
<li>Nädalapäev - (0-7). 0 ja 7 tähistavad pühapäeva</li>
</ul>

Tärn mingis väljas tähendab, et see vastab kõikidele väärtustele. Seega selle näite järgi, tahetakse, et skript käivituks iga päev igal kuul kell 8:30 hommikul.

Cronjob'i loomiseks tuleb vaid muuta crontab faili: <pre>crontab -e</pre>

## Harjutus

Luua mingi graafiku järgi aktiveeruv cronjob.

## Küsimus

Millise käsuga muudetakse croni tegumeid?

## Vastus

crontab -e
