# mv (Move)

## Tunni sisu

Kasutatakse failide liigutamiseks, aga ka ümbernimetamisek. Lippude ja toimimise poolest on see cp käsule üsna sarnane.

Faile saab ümbernimetada nii:

<pre>$ mv vanafail uusfail</pre>

Või sa võid liigutada faili hoopis teise kataloogi:

<pre>$ mv fail2 /home/pete/Dokumendid</pre>

Ja liigutada rohkem kui ühte faili:

<pre>$ mv fail_1 fail_2 /mingikataloog</pre>

Katalooge saab ka ümbernimetada:

<pre>$ mv kataloog1 kataloog2</pre>

Nagu ka cp, kui sa liigutad faili või kataloogi, siis see kirjutab samas kaustas teise samanimelise üle. Seega, kasuta -i lippu, et saaksid teate enne, kui midagi üle tahetakse kirjutada.

<pre>$ mv -i kataloog1 kataloog2</pre>

Aga ütleme, et sa isegi tahad liigutada faili nõnda, et see kirjutaks eelmise üle. Sa võid teha failist varuvariandi, sel juhul nimetatakse vana fail ümber ~ sümboliga.

<pre>$ mv -b kataloog1 kataloog2</pre>

## Harjutus

Anna mõnele failile uus nimi, seejärel liiguta see teise kataloogi.

## Küsimus

Kuidas sa annad failile nimega kass uue nime koer?

## Vastus

mv cat dog
