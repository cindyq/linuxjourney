# grep

## Tunni sisu

Grep on väga tõenäoliselt kõige tavalisem teksti töötlemise käsk, mida sa kasutama hakkad. See võimaldab otsida failist täemärke, mis vastavad teatud mustrile. Mis siis kui tahad teada, kas mingi fail eksisteerib mingis konkreetses kataloogis või, kas mingis failis asub mingi otsitav sõne? Kindlasti ei hakkaks sa kogu teksti läbi otsima, sa kasutaksid grep'i!

Kasutame näitena näide.txt faili:

<pre>$ grep rebane näide.txt</pre>

Peaksid nägema, et grep leidis sõna rebane failist näide.txt

Saab otsida ka väike- ja suurtähedele mittetundlikku teksti, kui kasutad lippu -i.

<pre>$ grep -i mingimuster mingifail</pre>

Et veelgi paindlikkust lisada, võib grep'i kombineerida teiste käskudega | operaatoriga.

<pre>$ env | grep -i Kasutaja</pre>

Nagu näha, on grep väga mitmekülgne. Mustris võib kasutada ka regulaaravaldisi:

<pre>$ ls /mingikat | grep '.txt$'</pre>

Peaks kuvama kataloogist mingikat kõik failid mis lõpevad .txt.

## Harjutus

Ehk oled kuulnud käskudest egrep ja fgrep, need on nüüd vananenud ning asendatud käskudega grep -E ja grep -F. Loe grep'i man lehekülge ja saad rohkem teada.

## Küsimus

Millist käsku kasutad, et mingit tähemärgi kombinatsiooni leida?

## Vastus

grep
