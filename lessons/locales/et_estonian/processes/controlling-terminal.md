# Kontrollterminalid

## Tunni sisu

Eelmises peatükis sai räägitud TTY väljast *ps*i väljundis. TTY on see terminal, mis käsu käivitas.

Terminale on kahte sorti: tavapärased <b>terminalid</b> ja <b>pseudoterminalid</b>. Tavapärane terminal on kohalik vahend, millesse saab trükkida ja saata väljund süsteemile. Kõlab justnagu terminali raknedus, mida oleme seni kasutanud, et käivitada kestaprogrammi, kuid päris nii see pole.

Liigume siit nüüd sujuvalt edasi, et seda demonstreerida. Kasuta klahvikombinatsiooni Ctrl-Alt-F1, et pääseda ligi virtuaalsele konsoolile TTY1. Kuvatakse ainult terminal, ei mingit graafikat. Seda nimetatakse tavapäraskes terminaliks. Seal saab väljuda klahvikombinatsiooniga Ctrl-Alt-F7.

Pseudoterminal on aga juba harjumuspäraseks saanud terminal, mis emuleerib terminali kestaprogrammi aknaga ja märgistus on PTS. Kui uuest vaadata *ps*i, siis kasutatav kesta protsess leitav pts/* alt.

Kui nüüd ringiga kontrollterminalide juurde tagasi tulla, siis protsessid ongi tavalieslt ühega seotud. Näiteks, kui sul kestaprogrammi aknas mingi protsess töötab ja see aken sulgeda, siis sulgub koos sellega too protsess.

On olemas spetsiaalsed protsessid, näiteks deemoni protsessid, mis hoiavad süsteemi käimas. Need käivituav tavaliselt süsteemi alglaadimisel ja peatuvad kui süsteem välja lülitada. Need protsessid töötavad taustal ja kuna me ei taha, et need peatuksid, siis ei ole need ka ühegi kontrollterminaliga seotud. *ps*i väljundis on TTY koha peal ?, mis tähendabki, et kontrollterminal puudub. 

## Harjutus

Vaadata *ps*i väljundit ja täheldada kõiki unikaalseid TTY väärtusi.

## Küsimus

Milline väärtus antakse protsessile, millel ei ole kontrollterminali?

## Vastus

?
