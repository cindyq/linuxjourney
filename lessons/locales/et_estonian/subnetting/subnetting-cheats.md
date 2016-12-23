# Alamvõrkude spikker

## Tunni sisu

See peatükk on natuke kahtlase väärtusega, kuna tõenäoliselt ei ole kunagi vaja käsitsi alamvõrke arvutada, kuid ütleme, et meid tabab äkitselt mingi selleteemaline intervjuu, siis oleks hea osata teisendada detsimaali ja binaari vahel. Õnneks on olemas aritmeetiline spikker, et sellega aidata.

Alustuseks tuleb õppida ära esimesed kahe astmed:

<ul>
<li>2^1 = 2</li>
<li>2^2 = 4</li>
<li>2^3 = 8</li>
<li>2^4 = 16</li>
<li>2^5 = 32</li>
<li>2^6 = 64</li>
<li>2^7 = 128</li>
<li>2^8 = 256</li>
<li>2^9 = 512</li>
<li>2^10 = 1024</li>
<li>2^11 = 2048</li>
<li>2^12 = 4096</li>
</ul>

<b>Detsimaalist binaari</b>

<pre>
1   1  1  1  1 1 1 1
128 64 32 16 8 4 2 1
</pre>

On väga palju põhjuseid, mis see graafik näeb välja just selline, huvi korral võib Internetist leida hulgaliselt materjale.

Jäi see kõik pähe? Nüüd siis kiire detsimaalist binaari teisendus:

<b>Teisendame binaaresitusse 192.168.23.43</b>

Meenutame: 128 / 64 / 32 / 16 / 8 / 4 / 2 / 1

Teeme koos läbi esimese okteti teisendamise ja see asi saab kiiresti selgeks.

<ol>
<li>Saame lahutada 192 - 128? Jah, seega esimene bitt on 1</li>
<li>192 - 128 = 64, järgmine number graafikus on 64, kas saame lahutada 64 - 64?Jah, seega teine bitt on 1</li>
<li>Kuna numbrid, mida lahutada, said otsa siis arvu 192 binaaresitus on 11000000</li>
</ol>

<b>Teisendame detsimaalesitusse 11000000</b>

Selleks liidame kokku need arvud, kus bitt on 1:

128 + 64 + 0 + 0 + 0 + 0 + 0 + 0 = 192!

## Harjutus

Tuvastada arvuti IP aadress ja alamvõrgu mask ning arvutada maksimaalne hostide arv enda võrgus.

## Küsimus

Kuidas on arvu 123 binaaresitus?

## Vastus

11111011
