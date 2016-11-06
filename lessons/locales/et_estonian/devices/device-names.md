# Seadmete nimed

## Tunni sisu

Mõned levinumad seadmete nimed:

<b>SCSI seadmed</b>

Massmäluseadmed kasutavad kõige tõenäolisemalt SCSI (hääldatakse "skazi") protokolli. SCSI tähendab *Small Computer System Interface*, mis tõlkes oleks väikearvutisüsteemi liides. Tegu on protokolliga, mida kasutatakse välisseadmete nagu kettad, printerid, skannerid ja muu ühendamiseks arvutiga. Eksisteerivad SCSI seadmed, mida kaasajal tegelikult enam ei kasutata, Linux aga samastab SCSI kettad /dev kataloogis füüsiliste kõvaketastega, mida nimetatakse ka plokkseadmeteks (*block device*) ja nende vaatamiseks käsk *lsblk*. Neid esindab eesliide *sd(SCSI disk):*

Tavapärased SCSI seadmefailid:

<ul>
<li>/dev/sda - Esimene kõvaketas</li>
<li>/dev/sdb - Teine kõvaketas</li>
<li>/dev/sda3 - Esimese kõvaketta kolmas kettajagu</li>
</ul>

<b>Pseudoseadmed</b>

Kordame, et pseudoseadmed ei ole tegelikult füüsiliselt arvutiga ühendatud ning enamik pseudoseadmeid on tähemärgiseadmed:

<ul>
<li>/dev/zero - võtab vastu ja heidab kogu sisendi kõrvale, väljundiks on NULL (nullväärtus) baitide jada</li>
<li>/dev/null - võtab vastu ja heidab kogu sisendi kõrvale  ning väljundit ei anna </li>
<li>/dev/random - toodab juhuslikke numbreid</li>
</ul>

<b>PATA seadmed</b>

Mõnikord, just vanemates süsteemides, võib näha, et kõvaketastele viidatakse hd prefiksiga:

<ul>
<li>/dev/hda - Esimene kõvaketas</li>
<li>/dev/hdd2 - Neljanda kõvaketta teine kettajagu</li>
</ul> 

## Harjutus

Kirjutada pseudoseadmetele, ning uurida väljundit. Ettevaatust, et ei kirjutaks nendele oma kettaid!

## Küsimus

Milline oleks tavaliselt teise SCSI ketta esimese kettajao seadmenimi?

## Vastus

sdb1
