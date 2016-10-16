# cd (Change Directory)

## Tunni sisu

Nüüd, kui sa tead, kus sa oled, vaatame, kas meil õnnestub failisüsteemis pisut ringi liikuda. Pea meeles, et liikumiseks peame kasutama asukohtade otsiteekondi. Asukoha määramiseks on kaks võimalust: absoluutne ja suhteline otsiteekond.

<ul>
<li>Absoluutne asukoht: See on faili asukoht alates juurkataloogist. Juur on meil see kõige olulisem tegelane. Juurkataloogi kuvatakse tavaliselt kaldkriipsuga. Kui asukoha alguses on /, siis tähendab, et sa alustad juurkataloogist. Näiteks /home/pete/Töölaud.</li>

<li>Suhteline asukoht: See on faili asukoht alates sinu praegusest asukohast failisüsteemis. Kui ma asuksin praegu /home/pete/Dokumendid ja tahaksin liikuda Dokumentides asuvasse arved kataloogi, siis ei ole mul vaja täpsustada kogu asukohta alates juurest, ma võin lihtsalt minna arved/ .</li>
</ul>

Nüüd, kui me teame kuidas asukohad toimivad, on meil vaja midagi, mis aitaks meil liikuda soovitud kataloogi. õnneks on meil cd või siis "muuda kataloogi", et seda saavutada.

<pre>$ cd /home/pete/Pildid</pre>

Nüüd ma muutsin oma asukohaks home/pete/Pildid.

Selles kaustas on mul aga katalaoog Hawaii, ma saan sinna liikuda nõnda:

<pre>$ cd Hawaii</pre>

Märkasid, et ma kasutasin ainult kausta nime? Sain nii teha, kuna mu asukoht juba oli /home/pete/Pildid.

Võib muutuda päris väsitavaks, kui kogu aeg peab kasutama absoluutseid või suhtelisi asukohti. Õnneks on meie abistamiseks olemas otseteed.

<ul>
<li>. (praegune kataloog). See on kataloog, milles sa asud. </li>
<li>.. (eelnev kataloog). Viib su praeguse kataloogi ülemkataloogi.</li>
<li>~ (home kataloog). See on vaikimisi su kodukataloog, näiteks /home/pete.</li>
<li>- (eelmine kataloog). Viib su kataloogi, kus sa viimati asusid.</li>
</ul>

<pre>$ cd .
$ cd ..
$ cd ~
$ cd -
</pre>
Proovi need ära!

<ol>
<li>Kuhu sa satud, kui sisestad cd käsu ilma täiendava infota?</li>
</ol>

## Küsimus

Kui su asukoht on /home/pete/Pildid ja sa tahad minna kataloogi /home/pete, siis millist otseteed oleks hea kasutada?

## Vastus

cd ..
