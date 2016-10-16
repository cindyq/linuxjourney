# cp (Copy)

## Tunni sisu

Teeme mõnest failist koopiad. Sarnaselt teistes operatsioonisüsteemides kopeerimisele ja kleepimisele, võimaldab kest meil seda teha isegi veel lihtsamalt.

<pre>$ cp minuvingefail /home/pete/Dokumendid/vingeddokud</pre>

minuvingefail on see fail, mida sa tahad kopeerida ja /home/pete/Dokumendid/vingeddokud on see, kuhu sa tahad seda kopeerida.

Sa saad kopeerida ka korraga mitmeid faile ja katalooge ning kasutada metamärki. Metamärk on selline tähemärk, mis võib asendada mingil mustril põhinevat valikut, andes sulle otsimiseks rohkem vabadust. Sa võid pandlikkuse mõttes kasutada metamärke iga käsu juures.


<ul>
<li>* metamärkide metamärk, kasutatakse, et esinada ükskõik millist tähemärki või sõnet</li>
<li>? esindab ühte tähemäri</li>
<li>[] esindab ükskõik millist kantsulgudesse kirjutatud tähemärki</li>
</ul>

<pre>$ cp *.jpg /home/pete/Pildid</pre>

See käsk kopeerib kõik .jpg laiendiga failid sinu jooksvast kataloogist kataloogi Pildid.

Päris kasulik on kasutada ka -r lippu, see kopeerib tagasiulatuvalt kataloogis asuvad kataloogid ja failid.

Proovi kasutada cp käsku, et kopeerida Dokumentide kausta mõni kataloog, milles on failid sees. See ei töötanud, eks? Seda selle pärast, et kopeerima peab ka kõik failid ja kataloogid, mis seal kaustas on käsuga -r.

<pre>$ cp -r Kõrvits/ /home/pete/Dokumendid</pre>

Oluline on panna tähele, et kui sa kopeerid faili kataloogi, milles on sama nimega fail, siis see fail kirjutatakse üle kopeeritava failiga. See ei ole väga bueno, kui sul on seal midagi, mida sa ei taha kogemata ülekirjutada. Sa võid kasutada lippu -i (interaktiivne), et sult küsitaks nõusolekut enne, kui fail ülekirjutatakse.

<pre>$ cp -i minuvingefail /home/pete/Pildid</pre>

## Harjutus

Kopeeri mõnda faili, kuid ole ettevaatlik, et sa midagi olulist üle ei kirjutaks.

## Küsimus

Millist lippu on sul täpsustamiseks vaja, kui soovid kopeeria kataloogi?

## Vastus

-r
