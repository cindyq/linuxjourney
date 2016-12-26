# Umask

## Tunni sisu

Iga loodav fail saab endale vaikimisi komplekti õigusi. Kui peaks tekkima vajadus neid vaikimis määratavaid õigusi muuta, saab seda teha *umask* käsuga. Käsk kasutab numbriformaati.

Kuid õiguste lisamise asemel võtab *umask* neid hoopis ära.

<pre>
$ umask 021
</pre>

Ülemises näites ütleme, et me tahame, et uutele failidele antaks vaikimisi järgmised õigused: Kasutajatel on ligipääs kõigele, kuid gruppidelt võtame ära õiguse kirjutada ja teistelt kasutatelt võtame ära käivitamise õiguse. Vaikimisi on umask enamustel Linuxitel 022, mis tähendab kõiki õigusi kasutajale, kuid grupil ja teistel kasutajatel puudub kirjutamisõigus.

Kui *umask* käsk sisestada, antakse vaikimisi õigused kõikidele uutele failidele, mis luuakse. Kui aga on soov, et sätted oleksid püsivad, tuleb muuta alglaadimise faili (.profile), kuid sellest räägime natuke hiljem.

## Harjutus

<ol>
<li> Luua uus fail ja kontrollida selle õigusi.</li>
<li> Muuta umask'i ja luua veel üks uus fail.</li>
<li> Kontrollida taaskord uue faili õigusi, mida võib näha?</li>
</ol>

## Küsimus

Millise käsuga muudetakse vaikimisi failiõigusi?

## Vastus

umask
