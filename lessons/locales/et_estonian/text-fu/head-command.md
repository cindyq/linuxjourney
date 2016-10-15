# head

## Tunni sisu

Ütleme, et meil on väga pikk fail, meil on isegi mitu, mille hulgast valida, proovi cat /var/log/syslog. Sa peaksid nägema lehekülgede kaupa teksti.  Mis siis kui ma tahaksid näha ainult paari eimest tekstifaili rida? Seda saame teha käsuga head. Vaikimisi näitab head käsk sulle faili esimest 10 rida.

<pre>$ head /var/log/syslog</pre>

Sa saad ka muuta ridade arvu endale meelepärasemaks. Ütleme, et tahad näha hoopis esimest 15 rida.

<pre>$ head -n 15 /var/log/syslog</pre>

Lipp -n esindab ridade arvu.

## Harjutus

Mida teeb järgnev käsk ja miks?

<pre>$ head -c 15 /var/log/syslog</pre>

## Küsimus

Millist lippu kasutad, kui tahad muuta head käsuga vaadeldavate ridade arvu?

## Vastus

-n

