﻿# Nimeviidad
## Tunni sisu

Kasutame viimast infosõlmede näidet:


<pre>
pete@icebox:~$ ls -li
140 drwxr-xr-x 2 pete pete 6 Jan 20 20:13 Desktop
141 drwxr-xr-x 2 pete pete 6 Jan 20 20:01 Documents
</pre>

*ls* käsu kolmandast väljas on siiamaani sujuvalt üle lipsatud, kuid see kuvabki viitade arvu. Viitade arv see tähendab püsiviitade arvu. See ilmselt ei seostu hetkel millegagi, kuid kohe räägitakse viitadest lähemalt.

<b>Nimeviidad</b>

Windows operatsioonisüsteemis on olemas *shortcut*'id. Ned polegi muud kui failide aliased. Kui midagi teha originaaliga, võib *shortcut* potensiaalselt katki minna. Linuxis vastavad nendele nimeviidad, mis lubavad viidata failine selle nime põhjal. Teist tüüpi viidad Linuxis on püsiviidad, mis on ise mingid failid, millel on ühendus infosõlmega. Vaatame seda asja praktiliselt alustades nimeviitadega.
 
<pre>
pete@icebox:~/Desktop$ echo 'minufail' > minufail
pete@icebox:~/Desktop$ echo 'minufail2' > minufail2
pete@icebox:~/Desktop$ echo 'minufail3' > minufail3

pete@icebox:~/Desktop$ ln -s minufail minufailiviit
pete@icebox:~/Desktop$ ls -li
total 12
  151 -rw-rw-r-- 1 pete pete 7 Jan 21 21:36 minufail
93401 -rw-rw-r-- 1 pete pete 8 Jan 21 21:36 minufail2
93402 -rw-rw-r-- 1 pete pete 8 Jan 21 21:36 minufail3
93403 lrwxrwxrwx 1 pete pete 6 Jan 21 21:39 minufailiviit -> minufail
</pre>

On loodud nimeviit nimega minufailiviit mis viitab minufailile. Märkame, et hoolimata sellest, et nimeviidad on kõigest failid, mis viitavad failinimedele, määratakse neile infosõlme number. Kui muuta nimeviita, muutub ka fail ise. Infosõlme numbrid on failisüsteemi piires unikaalsed, mis thendab, et kahte ühesugust numbrit olla ei saa ning samuti ei saa viidata failile mõnes teises failisüsteemis tema infosõlme numbriga. Nimeviit aga ei kasuta seda numbrit vaid faili nime, mistõttu neid saab kasutada läbi erinevate failisüsteemide.

<b>Püsiviidad</b>

Püsiviida näide:

<pre>
pete@icebox:~/Desktop$ ln minufail2 minupüsiviit
pete@icebox:~/Desktop$ ls -li
total 16
  151 -rw-rw-r-- 1 pete pete 7 Jan 21 21:36 minufail
93401 -rw-rw-r-- 2 pete pete 8 Jan 21 21:36 minufail2
93402 -rw-rw-r-- 1 pete pete 8 Jan 21 21:36 minufail3
93403 lrwxrwxrwx 1 pete pete 6 Jan 21 21:39 minufailiviit -> minufail
93401 -rw-rw-r-- 2 pete pete 8 Jan 21 21:36 minupüsiviit
</pre>

Püsiviit loov uue faili, mis viitab samale infosõlmele, mistõttu kui ma muudan midagi minufail2's või minupüsiviidas, siis on muudatus nähtav mõlemas. Kui aga kustutada minufail2, on fail ikkagi minupüsiviida kaudu kättesaadav. Siin kohal tuleb mängu viitade arv. Viitade arv kajastab infosõlme püsiviitade arvu. Kui fail eemaldada, siis see number väheneb. Infosõlm ise kustutatakse siis kui kõik püsiviidad sellele on kustutatud. Värskelt loodud faili viitade arv on 1, kunainfosõlmele vastab ainult see fai. Erinevalt nimeviitades, püsiviidad ei  toimi läbi mitme failisüsteemi. Need on failisüsteemis unikaalsed.

<b>Nimeviida loomine</b>

<pre>
$ ln -s minufail minuviit</pre>

Et luua nimeviita, kasutatakse *ln* käsku koos võtmega -s (nagu sümboolne) ning täpsustatakse fail ja viida nimi.

<b>Püsiviida loomine</b>

<pre>
$ ln mingifail mingiviit</pre>

Sarnaselt nimeviida loomisele kui -s jätakse seekord ära.

## Harjutus

Harjutada viitade loomist. Kustutada ka mõned ning uurida tagajärgi.

## Küsimus

Millise käsuga luuakse nimeviit?

## Vastus

ln -s