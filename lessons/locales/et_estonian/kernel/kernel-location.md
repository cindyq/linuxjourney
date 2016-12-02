# Tuuma otsiteekond

## Tunni sisu

Mis juhtub kui paigaldada uus tuum? See lisab su süsteemi mõned failid, mis tavaliselt paiknevad /boot kataloogis.

Erinevate versioonide jaoks on mitmeid faile:

<ul>
<li>vmlinuz - linuxi tuum</li>
<li>initrd - ehk on veel meeles, initrd on ajutine failisüsteem, mida kasutatakse enne tuuma laadimist</li>
<li>System.map - sümbolite tabel </li>
<li>config - tuuma sätted, tuuma ise kompileerides, võib sätestada, milliseid mooduleid laetakse</li>
</ul>

Kui /boot kataloogis saab ruum otsa, võib alati nende failide vanu versioone kustutada või lihtsalt kasutada selleks paketihaldurit. Selles kasutas hooldustööde tegemisega tasub olla ettevaatlik, et ei kustataks kogemata kasutusel olevat tuuma.

## Harjutus

Minna boot kataloogi ja uurida seal olevaid faile.

## Küsimus

Kuidas nimetatakse tuuma kujutist /boot kataloogis?

## Vastus

vmlinuz
