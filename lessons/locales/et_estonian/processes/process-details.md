# Protsessi detailid

## Tunni sisu

Enne kui süveneda protsesside praktilise rakendamise poolele, peaks mõistma, mis nad on ja kuidas nad töötavad. See osa võib päris keeruliseks minna, kuna lähme päris asja tuumani. Kui pole soovi praegu asjasse süveneda, võib selle peatüki juurde soovi korral ka hiljem tagasi pöörduda.

Nagu ennegi mainitud on protsess programm, mis süsteemis töötab, täpsemalt öeldes eraldab süsteem programmile töötamise jaoks mälu, protsessorit ja sisendit/väljundit. Protsess on töötava programmi üks esinemine. Proovida järgmist: Avada kolm terminali akent, kahes neist käiviata <b>cat</b> ilma lippudeta. Kolmandas aknas aga käivita <b>ps aux | grep cat</b>. On näha kaks *cat*i protessi, hoolimata sellest, et need mõlemad pöörduvad ühe programmi poole.

Protsesside eest vastutab tuum. Kui käivitada programm, siis tuum laeb mälust programmi koodi, tuvastab ja määrab sellele vajalikud ressursid ning peab arvet kõikide protsesside üle, mis sellega seotud on:

<ul>
<li>Protsessi staatus</li>
<li>Ressursid, mida protsess kasutab ja vastu võtab</li>
<li>Protsessi omanik</li>
<li>Signal handling (sellest räägitakse hiljem lähemalt)</li>
<li>Ja põhimõtteliselt kõik muu ka</li>
</ul>

Kõik protsessid tahavad maitsta magusad ressursside pirukat, tuuma ülesanne on hoolitseda selle eest, et iga protsess saab just nii palju, kui vaja on. Kui protsess lõppeb, vabanevad ressursid mõne teise jaoks.     

## Harjutus

Selles peatükis harjutust ei ole.

## Küsimus

Mis haldab ja kontrollib protsesse?

## Vastus

tuum
