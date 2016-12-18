# CRON'i tööd

## Tunni sisu

Kuigi oleme rääkinud ressursside kasutusest, võiks olla hea hetk mainida toredat Linuxi tööriista CRON, mida kasutatakse tegumite ajastamiseks. On olemas teenus, mis võimaldab programmidel töötada just siis kui kasutaja on selle ajastanud. See on eriti kasulik näiteks siis kui kasutaja tahab regulaarselt korra päevas käivitada mingit skript.

Ütleme, et on olemas skript, mille otsiteekond on */home/pete/scripts/muuda_taustapilt*. Kasutaja kasutab seda igal hommikul, et muuta töölaua taustapildina kasutatavat pilti. Kuid igal hommikul peab seda skripti käsitsi käivitama. Selle asemel võiks aga luua CRON'i töö, mis käivitab skripti läbi CRON'i. Skripti käivitamise ja CRON'i töö aktiveerimise aeg määratakse kasutaja poolt.

<pre>30 08 * * * /home/pete/scripts/muuda_taustapilt</pre>

Väljad vasakult paremale on järgmised:
<ul>
<li>Minut - (0-59)</li>
<li>Tund - (0-23)</li>
<li>Kuupäev - (1-31)</li>
<li>Kuu - (1-12)</li>
<li>Nädalapäev - (0-7). 0 ja 7 tähistavad pühapäeva</li>
</ul>

Tärn mingis väljas tähendab, et see vastab kõikidele väärtustele. Seega selle näite järgi, tahetakse, et skript käivituks iga päev igal kuul kell 8.30 hommikul.

Kasutaja CRON'i töö loomiseks tuleb vaid muuta *crontab* faili: <pre>crontab -e</pre>

Kogu süsteemi CRON seadistatakse failis */etc/crontab* kuid seda ei ole soovitav muuta enne kui on täielikult aru saadud selle muutmise eripäradest. Kui seal tehakse viga siis ei käivitata ka teisi seal failis olevaid töid, mis aga on süsteemi jätkusuutlikuks toimimiseks vajalikud. Superkasutaja õigustes on soovitav oma CRON'i tööd panna kirja kataloogi */etc/cron.d/* - seal võib näiteks endanimelise faili tekitada ja siis on ka teistele masina haldajatele teada kelle CRON'i tööd need on. Lisainfot leiab aadressilt https://help.ubuntu.com/community/CronHowto

## Harjutus

Luua mingi graafiku järgi aktiveeruv CRON'i töö.

## Küsimus

Millise käsuga muudetakse kasutajapõhiseid CRON'i töid?

## Vastus

crontab -e
