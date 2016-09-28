# alias

## Tunni sisu

Mõnikord võib muutuda käskude sisestamine väga korduvaks, või on sul on vaja kirjutada väga pikka käsku mitu korda. Sellisel juhul oleks parem kasutada aliast. Käsule aliase loomiseks pead lihtsalt täpsustama aliase nime ja seostama selle käsuga.

<pre>$ alias foobar='ls -la'</pre>

Nüüd võid ls -ls asemel kirjutada foobar ja see käivitab käsu. Päris viisakas värk. Pea meelest, et aliased ei säili, kui pead arvuti taaskävitama. Selleks peab looma permanentse aliase:

<pre>~/.bashrc</pre>

või mõnda teise sarnasesse faili, kui soovid, et see säiliks ka pärst taaskäivitamist.

Aliase saab eemaldada unalias käsuga:

<pre>$ unalias foobar</pre>

## Harjutus

Loo mõned aliased ja eemalda need.

## Küsimus

Millise käsuga luuakse alias?

## Vastus

alias
