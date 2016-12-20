# Üldine logimine

## Tunni sisu

Kasutaja süsteemis on päris palju logifaile, enamus olulisi on leitavad kataloogist /var/log. Kõiki ei hakata selles peatükis tutvustama, kuid mõned olulisemad tulevad siiski jutuks.

Kaks üldist logifaili, mis annavad kasutajale aimu, mis süsteemis toimub on järgmised:

<b>/var/log/messages</b>

See logi sisaldab endast kõik mitte-kriitlised ja mitte-silumise teated. Kaasatud on teated, mis on logitud alglaadmise ajal (dmseg), auth, cron, daemon jpt. Väga kasulik uurimaks, kuidas arvuti käitub.

<b>/var/log/syslog</b>

See logib kõike peale auth teadete. Äärmiselt kasulik, kui käsil on vigade otsimine.

Nendest kahest logist peaks rohkem kui piisama, kui peaks tekkima vajadus süsteemi seisukorda uurida. Kui aga peaks tekkima vajadus mõne konkreetse logi komponendi järgi, on ka need eraldi logidena olemas.

## Harjutus

Vaadata /var/log/messages ja /var/log/syslog faile ning märgata nende erinevusi.

## Küsimus

Milline logi logib kõike peale auth teadete?

## Vastus

syslog
