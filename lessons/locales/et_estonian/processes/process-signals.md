# Signaalid

## Tunni sisu

Signaal on teade protsessile, et midagi on juhtunud.

<b<Signaalide eesmärk</b>

Signaalid on tarkvaralised katksetused ja neil on palju eesmärke:

<ul>
<li> Kasutaja saab kasutada spetsiaalseid terminali klahvikombinatsioone, et protsesse peatada, katkestada või ajutiselt peatada. </li>
<li>Ilmneb riistvaraline probleem ja tuum tahab protsessi sellest teavitada.</li>
<li>Ilmneb tarkvaraline probleem ja tuum tahab protsessi sellest teavitada.</li>
<li>Põhimõtteliselt on need protsesside suhtlemise viis.</li>
</ul>

<b>Signaali protsess</b>

Kui mõnest sündmusest genereerub signaal edastatakse see protsessile. Signaal on kuni pärale jõudmiseni ootavas olekus. Signaali peetakse kohale toimetatuks, kui protsess käivitatakse. Küll aga on protsessidel signaali maskid ja signaalide kohaletoimetamise saab blokeerida, kui see on nõnda täpsustatud. Kui protsess saab signaali, võivad juhtuda järgmised:

<ul>
<li>Signaali ignoreeritakse</li>
<li>Signaal "püütakse kinni" ja teostatakse vastavad toimingud</li>
<li>Protsess peatatase ennetähtaegselt, vastandina tavapärasele töö peatamise süsteemsele kutsele</li>
<li>Signaal blokeeritakse sõltuvalt signaali maskist</li>
</ul>

<b>Tavalisemad signaalid</b>

Iga signaali defineerib täisarvuline number (integer) ja sümboolne nimi kujul SIGxxx. Mõned tavalisemad signaalid on:

<ul>
<li>SIGHUP või HUP või 1: <i>Hangup</i>ehk kontrollterminali sulgumine</li>
<li>SIGINT või INT või 2: <i>Interrupt</i> ehk katkestamine</li>
<li>SIGKILL või KILL või 9: <i>Kill</i> ehk peatamine</li>
<li>SIGSEGV või SEGV või 11: <i>Segmentation fault</i> ehk segmenteerimise viga</li>
<li>SIGTERM või TERM või 15: <i>Software termination</i> ehk tarkvara tegevuse lõpetamine</li>
<li>SIGSTOP või STOP: <i>Stop</i></li>
</ul>

Kuna numbrid signaalidel varieeruvad, kasutatakse pigem nimesid.

Leidub signaale, mida ei saa blokeerida. Üks selline näide on SIGKILL signaal. KILL signaal hävitab protsessi.

## Harjutus

Harjutust pole.

## Küsimus

Millist signaali ei saa blokeerida?

## Vastus

SIGKILL