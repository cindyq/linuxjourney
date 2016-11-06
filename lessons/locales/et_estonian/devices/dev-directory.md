# /dev kataloog

## Tunni sisu

Seadmed vajavad arvutisse ühendamisel tavaliselt juhtprogramme, et korralikult töötada. Seadmete juhtprogrammidega saab tegeleda läbi seadme failide või seadmesõlmede, mis on tegelikult lihtsalt erilised failid, mis näevad välja nagu tavalised failid. Kuna seadmefailid on just nagu tavalised failid, saab nendega tegutsemiseks kasutada programme nagu *ls*, *cat* jne. Seadmete faile hoitakse tavaliselt kataloogis /dev. Kui seal sisestada *ls* võib näha suurt hulka erinevaid seadmefaile.

<pre>$ ls /dev </pre>

Mõnda seadet on siin kursustel juba kasutatud ka, näiteks /dev/null. Ühes peatükis sai /dev/null'le saadetud väljund, tuum teab rakendada seda seadet ja lihtsalt heita sisend kõrvale, väljundit ei tagastata.

Kui vanasti taheti lisada süsteemi seadmeid, võis lihtsalt lisada faili /dev kataloogi ja ta sinna ka unustada. Kui nüüd hästi järgi mõelda, siis taipab peagi, miks see ei ole eriti hea mõte. /dev kaust kuhjub täis staatilisi faile või seadmeid, mida on juba ammu uunedatud, kasutamine lõpetatud vms. Seadmetele määratakse seadmefail selles järjekorras, milles tuum nad leiab. Nii võib juhtuda, et iga kord kui süsteem taaskäivitada, on seadmel erinev seadmefail.

Õnneks enam sellist meetodit ei kasutata. Nüüd kasutame hoopis midagi muud, et lisada ja eemaldada seadmeid dünaamiliselt. Sellest räägitakse tulevates peatükkides.

## Harjutus

Uurida /dev kasuta sisu. Kas on märgata tuttavaid seadmeid?

## Küsimus

Kus hoitakse süsteemi seadmefaile?

## Vastus

/dev
