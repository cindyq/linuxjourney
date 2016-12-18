# Sisendi/väljundi seire

## Tunni sisu

Nii hästi, kui saab uurida protsessi koormust, saab teostada ka ketta kasutamise seiret. Selleks on käepärane tööriist <b>iostat</b>.

<pre>
pete@icebox:~$ iostat
Linux 3.13.0-39-lowlatency (icebox)     01/28/2016      _i686_  (1 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
           0.13    0.03    0.50    0.01    0.00   99.33

Device:            tps    kB_read/s    kB_wrtn/s    kB_read    kB_wrtn
sda               0.17         3.49         1.92     385106     212417
</pre>

Esimene osa on protsessori informatsioon:

<ul>
<li>%user - protsessori kasutamise protsent kasutaja tasemel (rakendused) </li>
<li>%nice - protsessori kasutamise protsent kasutaja tasemel ja kenaduse prioriteetidega</li>
<li>%system - protsessori kasutamise protsent süsteemi (tuuma) tasemel </li>
<li>%iowait - protsent, mille jooksul protsessor oli tegevusetu, kuid eksisteerisid sisned/väljund päringud </li>
<li>%steal - aeg, mis kulus virtuaalsel protsessoril mittevabatahtlikule ootamisele, kuni teenindati teisi virtuaalseid protsessoreid. </li>
<li>%idle - aeg, kui protsessor oli tegevusetu ja puudusid sisend/väljund päringud</li>
</ul>

Teine osa on ketta kasutamise kohta:

<ul>
<li>tps - Ülekannete arv sekundis. Ülekanne on seadmele suunatud sisend/väljund päring. Mitu loogilist päringut võib liita üheks sisend/väljund päringuks. Ülekanne on määramata suurusega.</li>
<li>kB_read/s - Seadmelt loetud andmete kogus kilobaitides sekundi kohta.</li>
<li>kB_wrtn/s - Seadmele kirjutatud andmete kogus kilobaitides sekundi kohta.</li>
<li>kB_read - Summaarne kilobaitide arv, mis seadmelt loeti.</li>
<li>kB_wrtn - Summaarne kilobaitide arv, mida seadmele kirjutati.</li>
</ul>

## Harjutus

Kasutada iostat'i ketta kasutuse kuvamiseks.

## Küsimus

Millise käsuga saab kuvada sisendi/väljundi ja protsessori kasutust?

## Vastus

iostat
