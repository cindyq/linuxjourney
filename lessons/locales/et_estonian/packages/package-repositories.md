# Tarkvarahoidlad

## Tunni sisu

Kuidas saavad Internetti üleslaetud pakettid ühtäkki kasutajate arvutitesse? Kas peab minema iga paketi leheküljele, laadima nad alla ja paigaldama? Tegelikult võib seda muidugi ka nii teha, kuid on olemas palju parem lahendus, mida nimetatakse paketivaramuteks. Need ongi lihtsalt kesksed hoidlad pakettide jaoks. On olemas palju varamuid, mis hoiavad palju pakette ja mis kõige parem, need on kõik ka Internetist leitavad, mis tähendab, et tobedaid paigaldamiskettaid pole üldse tarvis. Küll aga ei oska arvutid ise ilma kasutaja abita neid hoidlaid otsida.

Näiteks, ütleme, et kasutaja soovib oma arvutisse WackyWidgets tarkvara. WackyWidgets haldab ise enda pakettide varamuid. Varamutes on 10 pakettid: CoolWidget, SuperWidget jne. WackyWidget hoiab oma varamut aadressil http://download.widgets/linux/deb/.

Selle asemel, et minna veebilehele pakette allalaadima, võib öelda arvutile, kust tarkvara leida.

Operatsioonisüsteemi distributsioonidel on juba algselt mingisugesed heaks kiidetud allikad, kust süsteem saab peamised olulised paketid. Debiani puhul on selleks failiks <b>/etc/apt/sources.list</b>. Arvuti oskab otsida sealt erinevaid allikaid, sealjuures neid, mida kasutajad võivad olla lisanud.

## Harjutus

Selles peatükis harjutus ei ole.

## Küsimus

Kus asub Debiani süsteemis lähtefail?

## Vastus

/etc/apt/sources.list
