# Shell

## Tunni sisu

Maailm on su auster, no tegelikult on shell su auster. Mis asi on shell? See on põhimõtteliselt programm, mis võtab klaviatuurilt sinu sisestatud käsu ja saadab selle operatsioonisüsteemile täitmiseks. Kuisa oled kunagi kasutanud graafilist kasutajaliidest, siis sa oled ilmselt näinud programme nagu "Terminal" ja "Konsool". Need on kõigest programmid, mis käivitavad sulle shelli. Selle kursuse vältel õpime shelli võludest.

Sellel kursusel kasutame shelli programmi bash (Bourne Again shell). Peaaegu kõik Linuxi distributsioonid kasutavad vaikimisi bashi. Saadaval on ka teisi shelle, nagu ksh, zsh, tsch, kuid siin me nendesse ei süvene.

Asume siis kohe asja kallale! Sõltuvalt distributsioonist võib su käsurida pisut erineda, kuid suuremalt jaolt peaks see siiski alluma järgmisele formaadile:
<pre>username@hostname:current_directory
pete@icebox:/home/pete $</pre>

Märkasid $ sümbolit teate lõpus? Erinevatel shellidel näevad käsuread erinevad välja, meie puhul tähistab $ Bashi, Bourne'i või Korn shelli tavakasutajat. Kui sa kirjutad käsku, siis sa seda käsureamärki ei kirjuta, kuid tea, et see on seal olemas.

Alustame lihtsa käsuga, echo. Echo käsk trükib ekraanile teksti argumendi.

<pre>$ echo Hello World</pre>

## Harjutus

Proovi veel mõnda Linuxi käsku ja uuri nende väljundeid:

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Küsimus

Milline väljund kuvatakse ekraanile kui sa sisestad käsureale echo Hello World?

## Vastus

Hello World


