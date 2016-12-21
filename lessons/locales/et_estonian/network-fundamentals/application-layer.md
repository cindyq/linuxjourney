# Rakenduskiht

## Tunni sisu

Ütleme, et ma tahan saata Peetrile e-kirja. Läbime kõik TCP/IP kihid, et seda tegevuses jälgida.

Meenutame, et andmete edastamiseks kasutatakse pakette. Pakett koosneb päisest ja kehast. Päises on informatsioon selle kohta, kust ja kuhu andmed liiguvad, kehas on aga saadetavad andmed ise. Võrgus liikudes lisab iga kiht paketi päisesse natuke informatsiooni. Tasub ka teada, et iga kiht nimetab seda "paketti" natuke erinevalt. Transpordikihis kapseldatakse andmed segmenti ja andmevahetuskihis on tegu raamiga. Kuid samamoodi võib kasutada sõna pakett.

Teekond algab rekenduskihist. Kui saata e-kiri läbi e-kirja programmi, kapseldab admed rakenduskiht. Rakenduskiht suhtleb transpordikihiga läbi täpsustatud pordi, läbi mille andmed saadetakse. Tahame saata kirja kasutades rakenduskihi protokolli SMTP. Andmeid saatekase transpordiprotokolliga, mis avab ühenduse selle protokolli pordiga (SMTP kasutab porti 25). Seega saadame andmed läbi selle pordi transpordikihile, kus see kapseldatakse segmentideks.

## Harjutus

Harjutust pole.

## Küsimus

Millises kihis esitatakse andmepakette kastuajasõbralikul kujul?

## Vastus

rakenduskiht
