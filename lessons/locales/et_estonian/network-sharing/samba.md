# Samba

## Tunni sisu

Kuna arvutustehnika algusaegadel oli Windowsi masinatel vaja jagada faile Linuxi masinatega, sündis SMB (*Server Message Block* ehk serveri sõnumi plokk) protokoll. SMB'd kasutati failide jagamiseks Windows operatsioonisüsteemis (Mac'il on ka võimalik), hiljem aga puhastati ja optimeeriti seda ja see võttis CIFS (*Common Internet File System* ehk lihtne interneti failisüsteem) protokolli kuju.

Sambaks nimetatakse Linuxi haldusvahendeid töötamaks Linuxis CIFS'ga. Lisaks failidele saab jagada ka muid ressursse nagu näiteks printerid.

<b>Sambaga võrgus jagamise üles seadmine</b>

Käime üle peamised sammud, et jagada midagi läbi võrgu Windows masinaga:

<b>Samba paigaldamine</b>

<pre>$ sudo apt update
$ sudo apt install samba</pre>

<b>Setup smb.conf</b>

Samba sätted asubad failis /etc/samba/smb.conf. See fail peaks ütlema süsteemile, milliseid katalooge tuleb jagada, nende ligipääsu õigused ja muud seaded. Vaikimisi on smb.conf failis palju väljakommenteeritud koodi, mida võib kasutada näitena, et ise seadeid kirjutada.
 
<pre>$ sudo vi /etc/samba/smb.conf</pre>

<b>Sambale salasõna seadmine</b>

<pre>$ sudo smbpasswd -a [kasutajanimi]</pre>

<b>Jagatud kausta loomine</b>

<pre>$ mkdir /minu/kataloog/mida/jagada</pre>

<b>Samba teenuse taaskäivitamine</b>

<pre>$ sudo service smbd restart</pre>

<b>Jagatud materjalidele ligipääsemine läbi Windowsi</b>

Windowsis tuleb lihtsalt sisestada võrgu ühendus run käsuviibale: \\HOST\jagamisenimi

<b>Samba/WIndowsi jagatud materjalidele ligipääsemine läbi Linuxi</b>

<pre>$ smbclient //HOST/kataloog -U kasutaja</pre>

Samba pakettis on olemas ka tööriist nimega <b>smbclient</b>, mida saab kasutada igasuguste Windowsi või Samba jagatud materjalidele ligipääsemiseks. Kui ühendus on saavutatud saab ringi liikuda ja faile üle kanda.

<b>Kinnita Samba kataloog enda süsteemi</b>

Selle asemel, et faile üks haaval üle kanda, võib jagatud kataloogi lihtsalt enda süsteemi haakida.

<pre>$ sudo mount -t cifs serverinimi:kataloog haakepunkt -o kasutaja=kasutajanimi,pass=salasõna</pre>

## Harjutus

Seada üles jagamine Sambaga, kui seda veel pole. Avada smb.conf ja saada tuttavaks võimalike valikutega sätete failis.

## Küsimus

Milline on uusim protokoll failide ülekandmiseks Windowsi ja Linuxi vahel?

## Vastus

CIFS
