# expand ja unexpand

## Tunni sisu

Cut käsu peatükis oli meil näide.txt fail, milles oli kasutatud tabulaatorit. Tavaliselt peaks see olema märgatavalt näha, kuid mõned tekstifailid ei näita seda piisavalt hästi. Tabulaator ei pruugi olla parim eraldaja, mida tekstifailis kasutada.
Et muuta kõik oma tabulaatorid tühikuteks, kasuta expand käsku.

<pre>$ expand näide.txt</pre>

See käsk trükib väljundi, kus kõik tabulaatorid on muudetud grupiks tühikuteks. Et see väljund faili salvestada, kasuta väljundi ümbersuunamist, nagu all näidatud.

<pre>$ expand näide.txt > tulemus.txt</pre>

Vastandile expand käsule, saame muuta ka grupi tühikuid tabulaatoriks. Kasutame selleks käsku unexpand:

<pre>$ unexpand -a tulemus.txt</pre>

## Harjutus

Mis juhtun kui sisestad lihtsalt expand ilma faili sisendita?

## Küsimus

Millise käsuga muudetakse tabulaatorid tühikuteks?

## Vastus

expand
