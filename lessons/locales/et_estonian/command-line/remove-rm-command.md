# rm (Remove)

## Tunni sisu

Nüüd kui mulle tundub, et meil on liiga palju faile, eemaldaks mõned. Selleks, et faile eemaldada, kasutame rm käsku. Rm (inglise keeles remove ehk eemalda) käsku kasutatakse, et kustutada faile ja katalooge.

<pre>$ rm fail1</pre>

Ole rm kasutamisega ettevaatlik, sul ei ole maagilist prügikasti, kust hiljem eemaldatud faile välja õngitseda. Kui nad on läinud, siis on nad igaveseks läinud, seega ole tähelepanelik.

Õnneks on üles seatud turvameetmed, et päris igaüks ei saaks eemaldada olulisi faile. Kirjutamise vastu kaitstud failid küsivad sult kinnitust enne, kui sa nad ära kustutad. Samuti ei ole kirjutamise vastu kaitstud kataloogi niisama lihtne eemaldada.

Kui sind kõik see eelnev ei huvita, siis saad sa faile igal juhul eemaldada.

<pre>$ rm -f fail1</pre>

-f (inflise keeles force ehk jõuga) valik ütleb rm käsule, et see eemaldaks kõik failid hoolimata sellest, kas nad on kirjutuskaitstud või mitte. Seda ilma, et sult enne üle küsitakse (kui sul on selleks vastavad volitused).

<pre>$ rm -i fail</pre>

Sarnaselt teistele käskudele, annab lipu -i lisamine sulle enne faili või kataloogi kustutamist võimaluse valida, kas sa ikka soovid seda teha.

<pre>$ rm -r kataloog</pre>

Kataloogi ei saa niisama lihtsalt eemaldada, sul on vaja lisada lipp -r (rekursiivne), et eemaldatakse kõik failid ja alamkataloogid, mis seal olla võivad.

Kataloogi saab eemaldada rmdir käsuga.

<pre>$ rmdir kataloog</pre>

## Harjutus

<ol>
<li>Loo fail nimega -fail (ära unusta sidekriipsu!).</li>
<li>Eemalda see fail.</li>
</ol>

## Küsimus

Kuidas eemaldada fail nimega minufail?

## Vastus

rm minufail
