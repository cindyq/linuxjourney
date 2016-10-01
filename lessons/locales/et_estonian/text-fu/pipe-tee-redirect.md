# toru ja tee

## Tunni sisu

Nüüd hakkame natuke torustikuga tegelema. No mitte päris, aga pisut. Proovime käsku:

<pre>$ ls -la /etc</pre>

Sa peaksid nägema väga pikka nimekirja, mida on isegi natuke raske lugeda. Selle asemel, et seda faili suunata, kas ei oleks toredam, kui saaksime seda väljundit vaadata mõne teise käsga nagu less? Aga me saamegi!

<pre>$ ls -la /etc | less </pre>

Toru operaator |, mida esindab püstkriips, lugag meil saada mõne käsu stdout ja teha sellest teisele protsessile stdin. Meie näite puhul me võtsime ls -la /etc stdout'i ja siis suunasime <i>toruga</i> less käsule. Toru käsk on äärmiselt kasulik ja me jätkame selle kasutamist aegade lõpuni.

Aga kui ma tahan kirjutada oma käsu väljundi kahele erinevale voole? See on väimalik järgmise käsuga:

<pre>$ ls | tee pähklid.txt</pre>

SA peaksid nägema ls väljundit ekraanid ja kui sa avad pähklid.txt faili, peaksid sa nägema seal täpselt sama informatsiooni!
 

## Harjutus

Proovi järgmist käsku:
<pre>$ ls | tee pähklid.txt banaan.txt</pre>

## Küsimus

Milline sümbol esindab toruoperaatorit?

## Vastus

|