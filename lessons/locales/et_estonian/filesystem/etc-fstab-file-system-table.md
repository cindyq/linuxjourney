# /etc/fstab

## Tunni sisu

Kui tahame alglaadimisel automaatselt failisüsteemi külgehaakida, tuleb see lisada faili nimega /etc/fstab (hääldatakse "eff ess täb"), mis on lühend "failisüsteemi tabelist". Selles failis hoitakse püsivalt ühendatud failisüsteeme.

<pre>
pete@icebox:~$ cat /etc/fstab
UUID=130b882f-7d79-436d-a096-1e594c92bb76 /               ext4    relatime,errors=remount-ro 0       1
UUID=78d203a0-7c18-49bd-9e07-54f44cdb5726 /home           xfs     relatime        0       2
UUID=22c3d34b-467e-467c-b44d-f03803c2c526 none            swap    sw              0       0
</pre>

Iga rida esindab ühte failisüsteemi. Väljad on järgmised:

<ul>
<li>UUID - Seade ID</li>
<li>Haakepunkt - Kataloog, kuhu seade on ühendatud</li>
<li>Failisüsteemi tüüp</li>
<li>Valikud - teised ühendumise võimalused, vaata lisainfo jaoks *man* lehekülge</li>
<li>*Dump* - *dump* haldusvahend kasutab seda, et otsustada millal on vaja luua varukoopiat, see võiks olla vaikimisi 0</li>
<li>*Pass* - *fsck* kasutab seda, et ostustada, mis järjekorras failisüsteeme kontrollima peab. Kui väärtus on null siis failisüsteemi ei kotrollita</li>
</ul>

Kirje lisamiseks tuleb lihtsalt muuta /etc/fstab faili sisu kasutades ülaltoodud korrektset süntaksit. Selle faili muutmisega tasub olla ettevaatlik, selle ära rikkumisega on täitsa võimalik muuta oma elu natuke raskemaks.

## Harjutus

Lisada kõnealune USB pulk /etc/fstab'i. Kui arvuti taaskäivitada peaks see olema endiselt ühendatud.

## Küsimus

Millises failis hoitakse failisüsteemide ühendumise infot?

## Vastus

/etc/fstab
