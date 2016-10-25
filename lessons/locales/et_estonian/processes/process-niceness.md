# Kenadus

## Tunni sisu

Kui tegeleda arvutis mitmete asjadega, korraga on avatud ehk Chrome, MS Word või Photoshop, siis võib tunduda, et need protsessid töötavad kõik samal ajal, kui tegelikult see päris nii ei ole.

Protsessid kasutavad protsessorit ainult väikese osa ajast, seda nimetatakse time slice. Seejärel nad peatuvad millsekunditeks ja teised protsessid saavad oma killukese aega. Vaikimis toimub see ikka üks teise järel uuesti ja uuesti. Kõik protsessid saavad piisaalt killukesi aega kuni nad oma tööga valmis saavad. Tuum haldab kogu seda protsesside ümberlülitumist ja suurem osa ajast teeb seda ka väga edukalt.

Protsessid ise ei saa otsustada millal ja kui palju nad protsessori aega kasutada saavad. Kui kõik töötavad tavapäraselt, saavad nad kõik ka (enamvähem) võrdselt protsessori aega. On aga võimalus tuuma protsessi vaikimis algoritmi muutmiseks *nice*(tõlkes kena) väärtusega. Kenadus on küll veider nimi, kuid see tähendab, et protsessid saavad numbri, mis määrab nende prioriteedi protsessori jaoks. Suurem number tähendab, et protsess on kena ja tal on madalam prioriteet protsessori jaoks, väike või negatiivne number tähendab, et protsess ei ole väga kena ja tahab saada nii palju protsessori aega kui võimalik.

<pre>$ top</pre>

Tulp NI ongi protsessi kenaduse tase.

Kenaduse taseme muutmiseks võib kasutada *nice* ja *renice* käske:

<pre>$ nice -n 5 apt upgrade</pre>

*Nice*i kasutatakse uuele protsessile prioriteedi määramiseks. *Renice* muudab aga juba olemas oleva protsessi prioriteeti.

<pre>$ renice 10 -p 3245</pre>

## Harjutus

Millised protsessid ei ole eriti kenad ja miks?

## Küsimus

Kui on vaja anda protsessile suurem protsessori prioriteet, kas *nice* number peab olema suurem või väiksem?

## Vastus

väiksem
