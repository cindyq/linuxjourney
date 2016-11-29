# Ketta jaotamine

## Tunni sisu

Järgnevalt harjutame failisüsteemi praktilist poolt USB pulga peal. Ei tasu muretseda kui endal ühte käepärast ei ole, võib ka lihtsalt kaasa mõelda.

Esiteks on tarvis tekitada kettajaod. Selle jaoks on saadaval palju tööriistu:

<ul>
<li>fdisk - lihtne käsureapõhine tööriist, vaikimisi kasutab MBR'i kuid toetab ka GPT'd. Salvestab muudatused alles siis kui selleks vastav käsklus antakse.</li>
<li>parted - käsureapõhine tööriist, mis toetab nii MBR'i kui GPT'd. NB! Salvestab koheselt (automaatselt, küsimata) tehtud muudatused! Olla ettevaatlik!</li>
<li>gparted - parted'i graafiline versioon</li>
<li>gdisk - sisuliselt fdisk kuid toetab ainult GPT'd ja mitte MBR'i (MBR teisendatakse koheselt GPT tabeliks, millega andmed kustuvad kuna kettajagude tabel kirjutatakse üle - kui kohe programmist väljuda q ja Enter abil ja mitte salvestada siis muudatused ei jõustu). Salvestab muudatused alles siis kui selleks vastav käsklus antakse.</li>
</ul>

Meie kasutame *parted*'i enda kettajagude loomiseks. Ütleme, et ühendatud USB seadme nimi on /dev/sdb2.

*Parted* on väga võimas tööriist ning kettajagude loomisel tasuks olla ettevaatlik. Erinevalt teistest kettajagude loomise programmidest salvestab *parted* **koheselt** (automaatselt, küsimata) loodud kettajaod. Seetõttu tasub olla ettevaatlik ja näiteks virtuaalarvutis esmalt järgi proovida kus ei ole riski andmete kogemata kustutamiseks.

<b>Käivitame *parted*</b>

<pre>$ sudo parted</pre>

Sisenenud *parted* tööriista, võib sisestada käske seadme kettajagude loomiseks. Abiinfot saab tippides *help* ja vajutades *Enter*.

<b>Seadme valimine</b>

<pre>select /dev/sdb2</pre>

Seadmega töötamiseks, tuleb see valida nime järgi.

<b>Jooksva kettajagude tabeli kuvamine</b>

<pre>
(parted) print                                                            
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

Kuvatakse seadme saadavalolevad kettajaod. <b>*start*</b> ja <b>*end*</b> punktid tuvastavad, kus kettajagu asub. Neid tuleb täpselt valida. *end* tähistab kettajao lõppu ketta algusest, mitte *start* väärtusest nagu võiks arvata.

<b>Kettajagude loomine</b>
Esmalt tuleks valida ühikud, mida *start* ja *end* puhul (ja ka teiste käskude puhul) kasutada (saab igal ajal muuta), näiteks:
<pre>unit GiB</pre>
Võimalus on kasutada nii detsimaal- kui binaarühikuid (lisainfo *parted'i* sees: *help unit*).

<pre>mkpart primary 123 4567</pre>

Nüüd tuleb valida *start* ja *end* ning luua kettajagu. Tuleb ka täpsustada, millist tüüp kettajagu luuakse, vastavalt kasutatavale kettajagude tabelile (tavaliselt MBR või GPT).<br>
*start* ja *end* on asukohad kettal, nt 4GB või 10%. Negatiivsed väärtused tähendavad arvestamist ketta lõpust alates alguse poole. Kusjuures *end* tähistab kettajao lõppu ketta algusest, mitte *start* väärtusest nagu võiks arvata. Näiteks -1s tähistab täpselt viimast sektorit. *mkpart* tekitab kettajao ilma failisüsteemita.

<b>Kettajao suuruse muutmine</b>

Kui ruumist jääb puudu võib kettajagude suurusi ka muuta. Seda ei võimalda mitte iga kettajagude loomise programm kuid *parted* võimaldab.

<pre>resize 2 1245 3456</pre>

Tuleb valida kettajao number ja soovitavad *start* ja *end* punktid.

*Parted* on väga võimas tööriist ning kettajagude loomisel tasuks olla ettevaatlik. Erinevalt teistest kettajagude loomise programmidest salvestab *parted* **koheselt** (automaatselt, küsimata) loodud kettajaod. Seetõttu tasub olla ettevaatlik ja näiteks virtuaalarvutis esmalt järgi proovida kus ei ole riski andmete kogemata kustutamiseks.

## Harjutus

Luua USB kettale kettajaod nõnda, et pool kettast oleks ext4 ja teine pool vaba.

## Küsimus

Millise käsuga luuakse *parted* tööriistas uus kettajagu?

## Vastus

mkpart
