# Protsesside loomine

## Tunni sisu

See ja eelmine peatükk on puhtalt informatiivsed, et tutvustada natuke kapotialust. Võid igal ajal siia tagasi pöörduda, kui oled juba veidi rohkem protsesside kallal töötanud.

Protsessi loomisel põhimõtteliselt kloonitakse juba olemasolevat protsessi kasutades midagi, mida nimetatakse *fork* süsteemseks kutseks (süsteemsetest kutsetest räägitakse alles väga kauges tulevikus). *Fork* kutse loob olmeasolevale protsessile identse tütarprotsessi, mis võtab endale uue protsessi ID (PID) ja esialgsest protsessist saab emaprotsess, mis saab endale emaprotsessi ID <b>PPID</b>. Hiljem võib aga tütarprotsess jätkata sama programmi kastuamist, mida kasutas tema ema või kasutada *execve* süsteemset kutset, et käivitada uus programm. See kutse hävitab senise tuuma poolt selle protsessi jaoks loodud mälu haldamise ning seab üles uued just selle programmi jaoks.

Seda võib tegevuses näha:

<pre>$ ps l</pre>

Valik l (nagu *long format* ehk pikk formaat) võimaldab jooksvaid protsesse vaadeleda isegi veel detailsemalt. Näha on tulp nimega <b>PPID</b>, see ongi ema ID. Kui nüüd vaadata oma terminali, siis on näha protsess, mis on jooksev kestaprogramm, näiteks *bash*. Meenuta, et kui sisestasid *ps l* käsu, käivitasid sa selle protsessist, mis käitas *bash*i. Märka, et *bash*i kesta <b>PID</b> on selle *ps l* käsu <b>PPID</b>.

Seega, kui igal protsessil peab olema ema ja kõik protsessid on üksteise harud, peab ju kusagil olema kõikide protsesside ema, eks? Nii ongi. Kui süsteem algkäivitub, loob tuum protsessi nimega <b>init</b>, mille PID on 1. Seda protsessi saab peatada vaid siis kui süsteem välja lülitada. *Init* jookseb juurkasutaja õigustes ja käitab mitmeid teisi protsesse, mis võimaldavad süsteemil töötada. *Init* tuleb lähema vaatluse alla süsteemi algkäivitamise kursusel, praegu võiks meelde jätta, et tegu on kõikide teiste protsesside loojaga.

## Harjutus

Kui vaadata töötavaid protsesse, millistel protsessidel veel on emad?

## Küsimus

Milline süsteemi kutse loob uue protsessi?

## Vastus

fork
