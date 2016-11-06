# Seadmete nimed

## Tunni sisu

Mõned levinumad seadmete nimed:

<b>SCSI seadmed</b>

Massmäluseadmed kasutavad kõige tõenäolisemalt SCSI (hääldatakse "skazi") protokolli. SCSI tähendab *Small Computer System Interface*, mis tõlkes oleks väikearvutisüsteemi liides. Tegu on protokolliga, mida kasutatakse välisseadmete, nagu kettad, printerid, skännerid ja muu, ühendamiseks arvutiga. Eksisteerivad SCSI seadmed, mida kaasajal tegelikult enam ei kasutata, Linux aga samastab SCSI kettad /dev'is kõvaketastega. Neid esindab prefiks *sd(SCSI disk):*

Tavapärased SCSI seadme failid:

<ul>
<li>/dev/sda - Esimene kõvaketas</li>
<li>/dev/sdb - Teine kõvaketas</li>
<li>/dev/sda3 - Esimese kõvaketta kolmas kettajagu</li>
</ul>

<b>Pseudoseadmed</b>

Kordame, et pseudoseadmed ei ole tegeleikult füüsiliselt arvutiga ühendatud ning enamik pseudoseadmeid on tähemärgiseadmed:

<ul>
<li>/dev/zero - võtab vastu ja heidab kogu sisendi kõrvale, väljundiks on NULL (nullväärtus) baitide jada</li>
<li>/dev/null - võtab vastu ja heidab kogu sisendi kõrvale  ning väljundit ei anna </li>
<li>/dev/random - toodab juhuslikke numbreid</li>
</ul>

<b>PATA seadmed</b>

Mõnikord, just vanemates süstemides, võib näha, et kõvaketastele viidatakse hd prefiksiga:

<ul>
<li>/dev/hda - Esimene kõvaketas</li>
<li>/dev/hdd2 - Neljanda kõvaketta teine kettajagu</li>
</ul> 

## Harjutus

Kirjutada pseudoseadmetele, ning uurida väljundit. Ettevaatust, et ei krijutaks nendele oma kettaid!

## Küsimus

Milline oleks tavaliselt teise SCSI ketta esimese kettajao seadmenimi?

## Vastus

sdb1
