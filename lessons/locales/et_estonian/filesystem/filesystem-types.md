# Failisüsteemi tüübid

## Tunni sisu

Saadava on suur hulk erinevaid failisüsteemi teostusi. Mõned on kiiremad kui teised, mõned toetavad suuremaid mälumahte, teised töötavad ainult väiksematega. Erinevad failisüsteemid korrastavad andmeid erinevalt, sellel kursusel tutvustatakse erivaid tüüpe detailselt. Kuna erinevaid teostusi on saadaval palju, peavad rakendused kõiksuguste erinevate toimingutega kohanduma. On olemas selline asi, nagu virtuaalne failisüsteemi (VFS) abstraktsiooni kiht. See on kiht rakenduste ja erinevate failisüsteemi tüüpide vahel, milletõttu ei tee vahet millist failisüsteemi kasutada, rakendused tulevad ikka toime.

Tulevates peatükkides räägime kettajagudest, mis võimaldavad ühel kettal rakendada mitmeid erinevaid failisüsteeme.

<b>Logiga failisüsteem</b>

Logimine on tavaliselt vaikimisi kõikides failisüsteemi tüüpides olemas ja isegi kui ei ole, peaks teadma, mis selle funktsioonid on. Ütleme, et käsil on suuremahulise faili kopeerimine kui äkitselt kaob vool. Kui kasutada mittelogivat failisüsteemi, oleks kopeeritav fail vigane ja failisüsteemis puuduks järepidevus. Kui arvuti uuesti käivitada kontrollitakse failisüsteemi, et kõik oleks korras. Parandustööd võivad aga üsna palju aega võtta, sõltuvalt failisüsteemi suurusest muidugi.

Kui aga kasutada logivat failisüsteemi, kirjutatakse veel enne kui üldse midagi kopeerima hakatakse, alustatav tegevus logifaili. Kui kopeerimine valmis saab, tehakse ka logisse vastav märge. Tänu sellisele mehhanismile on andmed failisüsteemis kogu aeg kooskõlas ning süsteem teab täpselt, kus kasutajal töö pooleli jäi kui vool peaks ootamatult kaduma. Ka käivitumise aeg on sedasi lühem, kuna selle asemel, et kontrollida kogu süsteemi, kontrollitakse vaid logi.

<b>Tavalisemad lauaarvuti failisüsteemi tüübid</b>
 
<ul>
<li>ext4 - Linuxile omaste failisüsteemide käesolev versioon, mis on ühilduv oma eelkäijate ext2 ja ext3 versioonidega. See toetab ketta mahtusid kuni 1 exabait ja faili suurusi kuni 16 terabaiti jpm. </li>
<li>Btrfs - "*Better* või *Butter FS*" on Linuxis uus failisüsteem, millega tulevad kaasa hetktõmmised, varundamine, paranenud jõudlus jpm. See on laialdaselt kättesaadav kuid mitte veel lõpuni stabiilne või ühilduv. </li>
<li>XFS - Kõrge jõudlusega logiga failisüsteem. Hea suurte failidega süsteemidele, näiteks meediaserverid.</li>
<li>NTFS ja FAT - Windows'i failisüsteemid</li>
<li>HFS+ - Macintosh'i failisüsteem</li>
</ul> 

Nii saab uurida arvutis kasutatavaid failisüsteeme:

<pre>
pete@icebox:~$ df -T
Filesystem     Type     1K-blocks    Used Available Use% Mounted on
/dev/sda1      ext4       6461592 2402708   3707604  40% /
udev           devtmpfs    501356       4    501352   1% /dev
tmpfs          tmpfs       102544    1068    101476   2% /run
/dev/sda6      xfs       13752320  460112  13292208   4% /home
</pre>

<b>df</b> käsk kuvab muu hulgas informatsiooni ketaste mahtude kasutamise kohta. Sellest tööriistast räägitakse hiljem veel.

## Harjutus

Uurida Internetist ka teiste failisüsteemide kohta: ReiserFS, ZFS, JFS ja muud, mida võib leida.

## Küsimus

Milline on tavaline Linuxi failisüsteemi tüüp?

## Vastus

ext4
