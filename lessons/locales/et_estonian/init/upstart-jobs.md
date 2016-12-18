# Upstart'i tegumid

## Tunni sisu

*Upstart* võib algatada palju sündmusi ja tegumeid, paraku aga ei ole kerge tuvastada, kust midagi neist pärineb. Selleks tuleb natuke sobrada kataloogis /etc/init. Suurema tõenäosusega pole kasutajal aga kunagi vaja *Upstart*'i sätete faile vaadata, kuid need võimaldavad soovi korral mingeid spetsiifilisi tegumeid paremini kontrollida. *Upstart* süsteemis on võimalik kasutada hulgaliselt kasulikke käske.

<b>Tegumite kuvamine</b>

<pre>initctl list

shutdown stop/waiting
console stop/waiting
...
</pre>

Kuvatakse nimekiri *Upstart*'i tegumitest neile rakendatud erinevate olekutega. Igal real on tegumi nimi esimene väärtus, teine väli (enne /) on tegumi sihtkoht. Kolmas väärtus (/ järel) on hetke olek. Kasutaja võib näha, et süsteemi sulgemise tegum tahab mingil hetkel lõpetada, kuid on hetkel ootavas olekus. Tegumi olek ja sihtkoht muutuvas tegumeid käivitades ja sulgedes.

<b>Kuva konkreetne tegum</b>

<pre>initctl status networking
networking start/running
</pre>

Siin kursusel ei minda *Upstart*'i tegumite seadete kirjutamise oskuse osas detailidesse, kuid juba on tutvustatud, et nende seadete kaudu tegumeid alustatakse, peatatakse ja taaskäivitatakse. Tegumitest võivad käivituda ka teised tegumid. Olulisemad *Upstart*'i manuaalsed käsud käiakse siinkohal üle, kuid kui huvi on suurem peaks uurima lähemalt  .conf faile.

<b>Käivita tegum käsitsi</b>

<pre>$ sudo initctl start networking</pre>

<b>Peata tegum käsitsi</b>

<pre>$ sudo initctl stop networking</pre>

<b>Taaskäivita tegum käsitsi</b>

<pre>$ sudo initctl restart networking</pre>

<b>Emiteeri tegum käsitsi</b>

<pre>$ sudo initctl emit some_event</pre>

## Harjutus

Kuvada *Upstart* tegumite nimekiri. Muuta mõne tegumi olekut äsja õpitud käskudega. Mida võib selle tagajärjel märgata?

## Küsimus

Kuidas käsitsi taaskäivitada tegum nimega moos?

## Vastus

sudo initctl restart moos
