# Logifailide haldamine

## Tunni sisu

Logifailid toodavad palju andmeid ja neid andmeid hoitakse kasutaja kõvakettal. Sellega seoses tekivad probleemid. Enamast soovib kasutaja näha uuemaid logisid, samuti tahetakse hallata kettaruumi efektiivselt. Kuidas seda aga teha? Vastus on haldusvahendis logrotate.

Logrotate haldab kasutaja eest tema logifaile. Sätete failis saab täpsustada kui palju ja milliseid logisid alles hoida, kuidas nende mahtu vähendada, et kettaruumi säästa ja palju muud. Logrotate käivitatakse tavaliselt läbi cron'i korra päevas ning selle sätete fail asub /etc/logrotate.d.

Logrotate'ile sarnaseid tööriistu, millega logisid hallata leidub veel, kui logrotate on kõige levinum.

## Harjutus

Tutvuda logrotate sätete failiga ning tuvastada, kuidas see haldab mõningaid logisid.

## Küsimus

Milline on levinuim logide haldamise vahend?

## Vastus

logrotate
