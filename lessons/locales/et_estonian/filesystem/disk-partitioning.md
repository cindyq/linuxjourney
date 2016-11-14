# Ketta jaotamine

## Tunni sisu

Järgnevalt harjutame failisüsteemi praktilist poolt USB pulga peal. Ei tasu muretseda, kui endal ühte käepärast ei ole, võib ka lihtsalt kaasa mõelda.

Esiteks on tarvis tekitada kettajaod. Selle jaoks on saadaval palju tööriistu:

<ul>
<li>fdisk - lihtne käsureapõhine tööriist, ei toeta GPT'd</li>
<li>parted - see käsureapõhine tööriist toetab nii MBR'i kui GPT'd</li>
<li>gparted - *parted*'i graafiline versioon</li>
<li>gdisk - fdisk, kuid toetab ainult GPT'd ja mitte MBR'i</li>
</ul>

Meie kasutame *parted*'i enda kettajagude loomiseks. Ütleme, et ühendatud USB seadme nimi on /dev/sdb2.

<b>Käivitame *parted*</b>

<pre>$ sudo parted</pre>

Sisenenud *parted* tööriista, võib sisestada käske seadme partitsioonide loomiseks.

<b>Seadme valimine</b>

<pre>select /dev/sdb2</pre>

Seadmega töötamiseks, tuleb see valida nime järgi.

<b>Jooksva partitsioonitabeli kuvamine</b>

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

Kuvatakse seadme saadavalolevad partitsioonid. <b>*start*</b> ja <b>*end*</b> punktid tuvastavad, kus kettajagu täpselt asub. Neid tuleb hästi valida.

<b>Kettajagude loomind</b>

<pre>mkpart primary 123 4567</pre>

Nüüd tuleb valida *star* ja *end* ning luua kettajagu. Tuleb ka täpsustada, millist tüüp partitsioon luukase, vastavalt kasutatavale tabelile.

<b>Kettajao suuruse muutmine</b>

Kui ruumist jääb puudu võib kettajagude suurusi ka muuta.

<pre>resize 2 1245 3456</pre>

Tuleb valida partitsiooni number ja soovitavad *star* ja *end* punktid.

*Parted* on väga võimas tööriist ning kettajagude loomisel tasuks olla ettevaatlik.

## Harjutus

Luua USB kettale kettajaod nõnda, et pool kettast oleks ext4 ja teine pool vaba.

## Küsimus

Millise käsuga luuakse *parted* tööriistas uus kettajagu?

## Vastus

mkpart
