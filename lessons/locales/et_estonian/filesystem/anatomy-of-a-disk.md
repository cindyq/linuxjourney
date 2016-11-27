# Ketta anatoomia

## Tunni sisu

Kõvakettaid saab jagada kettajagudeks, luues nõnda blokkseadmeid. Meenutame seadmeid /dev/sda1 ja /dev/sda2, /dev/sda on üks terve ketas, kuid /dev/sda1 on selle ketta esimene jagu. Kettajaod on äärmiselt kasulikud andemete eraldamiseks. Kui on tarvis mingit konkreetset failisüsteemi kasutada, võib kerge vaevaga luua kettale jao, selle asemel, et kogu kettale seda ühte failisüsteemi rakendada.

<b>Partitsioonitabel</b>

Igal kettal on partitsioonitabel, mis edastab süsteemile infot ketta jaotamise kohta. Seal on info selle kohta, kus kettajagu algab ja lõppeb, millised jaod on alglaetavad, millised sektorid on millistele jagudele määratud jne. Kasutatakse kahte põhilist partitsioonitabelit: *Master Boot Record* (MBR) ja *GUID Partition Table* (GPT).

<b>Kettajagu ehk partitsioon</b>

Kettajagudest koosnevad kettad võimaldavad organiseerida andmeid. Kui kettal on mitmeid partitsioone, ei tohi need omavahel kattuda. Kui kettal on ala, mis ei kuulu kettajao alla, nimetatakse seda vabaks alaks. Partitsiooni tüüp sõltub partitsioonitabelist. Kettajaol võib olla failisüsteem, või võib seda kasutada muul otstarbel, näiteks  saalimiseks (sellest räägitakse ka varsti).

<i>MBR</i>

<ul>
<li>Traditsiooniline partitsioonitabel, kasutatud kui standardit</li>
<li>Võimaldab primaarseid, laiendatud ja loogilisi kettajagusid</li>
<li>MBR piiranguks on kuni neli primaarset kettajagu</li>
<li>Täiendavaid partitioone saab luua muutes primaarne kettajagu laiendatuks (lubatud on ainult üks laiendatud kettajagu). Selle sisse saab omakorda luua loogilisi partitsioone.</li> 
<li>Toetatud on kuni 2 terabaidised kettad</li>
</ul>

<i>GPT</i>

<ul>
<li>*GUID Partition Table*ist (GPT) on saamas kettajagude vallas uus standard</li>
<li>Koosseisu kuuluvad vaid ühte tüüpi kettajaod, mida võib luua hulgaliselt</li>
<li>Igal kettajaol on globaalselt unikaalne ID (GUID)</li>
<li>Kasutatakse peamiselt koos UEFI põhise alglaadimisega (detailsemalt tuleb sellest juttu hilisemal kursusel)</li> 
</ul>

<b> Failisüsteemi struktuur</b>

Eelmisest peatükist on teada, et failisüsteem on failide ja kataloogide organiseeritud kogum. Kõige lihtsamalt võib seda vaadelda kui kooslust andmebaasist, mis haldab faile ja andmed ise. Kuid nüüd süveneme sellesse väheke detailsemalt.

<ul>
<li>Alglaadimise blokk - See asub failisüsteemi esimestes sektorites. Seda otseselt ei kasutata, vaid hoiab informatsiooni operatsiooni alglaadimise jaoks. Selliseid blokke on operatsiooni süsteemil tarvis vaid ühte. Kui partitsioone on rohke, leidub ka neil algalaadimise blokk, kuid paljusid ei kasutata.</li>
<li>Superblokk - Üksik blokk, mis järgneb kohe alglaadimisblokile. Sisaldab infot failisüsteemi kohta: infosõlmetabel, loogiliste jagude ja failisüsteemi suurus. </li>
<li>Infosõlmede tabel - Sellest võib mõelda kui andmebaasist, mis haldab andmeid (ei tasu muretsed, sellest tuleb terve peatükk). Iga faili või kataloogi kohta on selles tabelis unikaalne kirje. Failide kohta hoitakse erinevat informatsiooni. </li>
<li>Andmeblokid - Failide ja kataloogide tegelikud andmed </li>
</ul>

Tutvume erinevate partitsioonitabelitega. All on näide kettajaost, mis kasutab MBR partitsioonitabelit (msdos). Kergesti on eristatavad primaarne, laiendatud ja loogilised kettajaod.

<pre>
pete@icebox:~$ sudo parted -l
Model: Seagate (scsi)
Disk /dev/sda: 21.5GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos

Number  Start   End     Size    Type      File system     Flags
 1      1049kB  6860MB  6859MB  primary   ext4            boot
 2      6861MB  21.5GB  14.6GB  extended
 5      6861MB  7380MB  519MB   logical   linux-swap(v1)
 6      7381MB  21.5GB  14.1GB  logical   xfs
</pre>

GPT kasutab kettajagudel ainult unikaalseid ID'sid.

pre>
Model: Thumb Drive (scsi)
Disk /dev/sdb: 4041MB
Sector size (logical/physical): 512B/512B
Partition Table: gpt

Number  Start   End     Size     File system  Name        Flags
 1      17.4kB  1000MB  1000MB                first
 2      1000MB  4040MB  3040MB                second
</pre>

## Harjutus

Sisestada käsk <b>parted -l</b> ja hinnata tulemust.

## Küsimus

Millist kettajao tüüpi peaks kasutama, et luua rohkem kui 4 partitsiooni MBR skeemi järgi?

## Vastus

laiendatud
