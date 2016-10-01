# stdout (Standard Out)

## Tunni sisu

Praguseks oleme juba päris paljude käskude ja nende väljunditega tuttavaks saanud ja see viib meid ka edasi järgmise teemani: sisend/väljund vood. Sisestame järgmise käsu ja pärast arutame, kuidas see töötab:

<pre>$ echo Hello World > pähklid.txt</pre>

Mis just praegu juhtus? Aga mine kontrolli seda kataloogi, kus käsk käivitati ja pane end valmis, sest sa peaksid sealt leidma faili nimega pähklid.txt. Kui sa sinna sisse vaatad, siis peaksid leidma teksti Hello World. Selle ühe käsuga juhtus päris palju, vaatame seda jupp haaval.

Vaatame esimest osa:

<pre>$ echo Hello World</pre>

Me teame, et see trükib ekraanile Hello World, aga kuidas? Protsessid kasutavad sisend-väljund voogusid, et võtta vastu sisendandmeid ja väljastada väljundeid. Vaikimisi võtab echo käsk sisendi (standard sisend või stdin) klaviatuurilt ja tagastab väljundi (standard väljund või stdout) ekraanile. Seepärast, kuvatakse su ekraanile Hello World, kui sa sisestad kesta echo Hello World. Sisend-väljundi ümbersuunamisega saame aga seda vaikimisi käitumist muuta, see annab meile failide osas suurema paindlikuse.

Vaatame, mis käsuga edasi juhtus:

<pre> > </pre>

> on ümbersuunamise operaator, mis laseb meil muuta seda, kuhu suunatakse standardväljund. See lubab meil suunata echo Hello Worldi väljundi ekraani asemel faili. Kui sellist faili veel olemas ei ole, siis see luuakse. Kui see aga on olemas, siis kirjutatakse see üle (olenevalt kestast, saad sa lisada käsule lipu, et sellist olukorda vältida).

Ja nii põhimõtteliselt stdout ümbersuunamine töötabki!

Ütleme aga, et ma ei taha oma pähklid.txt faili ülekirjutada. Õnneks on selle jaoks ja olemas ümbersuunamise operaator, >>:


<pre>$ echo Hello World >> pähklid.txt</pre>

See lisab Hello Worldi pähklid.txt faili lõppu. Kui aga faili eelnevalt ei eksisteerinud, siis luuakse see, justnagu > ümbersuunamise puhulgi.


## Harjutus

Proovi paari käsku:

<pre>
$ ls -l /var/log > minuväljund.txt
$ echo Hello World > rm
$ > mingifail.txt 
</pre>

## Küsimus

Millist käsku kasutad kui tahad väljundi lisada olemasoleva faili lõppu?

## Vastus

>>
