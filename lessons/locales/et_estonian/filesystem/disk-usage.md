# Kettakasutus

## Tunni sisu

Kettakasutuse kuvamiseks on mõned tööriistad:

<pre>
pete@icebox:~$ df -h
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/sda1       6.2G  2.3G  3.6G  40% /
</pre>

df käsk kuvab kettakasutuse hetkel ühendatud failisüsteemide kohta. Parameeter -h vormuleerib väljundi inimloetavaks. Kuvatakse seade ja kui palju mahust on veel kasutamata.

Ütleme, et ketas hakkab täis saama ning tahetakse teada, millised failid või kataloogid võtavad palju ruumi. Selleks on käsk <b>du</b>.

<pre>$ du -h</pre>

Käsk kuvab hetke asukohta kataloogi kasutusinfo. Juurkataloogi piilumiseks võib kasutada <b>du -h /</b>, kuid see väljund võib osutuda natuke liiga mahukaks.

Mõlema käsu süntaks on teineteisele nii sarnane, et võib osutuda raskeks pidada meeles, kumba kasutada. Inglisekeele oskajaid aitab pidada meeles, et vaba kettaruumi näitab *<b>disk</b> is <b>free</b>* ehk df ja kasutatud kettaruumi *<b>disk usage</b>* ehk du.  

## Harjutus

Kasuta du ja df käske, et uurida kasutatud ja vaba ruumi.

## Küsimus

Milline käsk kuvab kettal vaba ruumi?

## Vastus

df
