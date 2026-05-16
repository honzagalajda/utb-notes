# Analýza před zkouškou z DC

Zkouška probíha tak, že dostaneš 2 témata a máš 40 min. na to, abys napsal co víš. Pak jdeš ven ze zkouškové místnosti. Postupně si lidi volá, opravuje to co máš na papíře a doptává se na otázky. Když je známka nerozhodná může se zeptat i na _doplňující_ otázku mimo téma. Ústní část trva 15-20 min.

Ke zkoušce je třeba si vzít **psací potřeby, papíry a průkaz studenta**.

Prý je ideální popsat jednu stranu A4 na jedno téma...

Učitel si potrpí na tom, ať je vše popsáno dopodrobna.

Na DC lidi říkají, že z té úvodní prezentace (historie, atd..) tam nic nebude. Taky říkají, že se stačí dopodrobna naučit z prezentací. Jeden týpek dostal takto i za A :D

Dává i mínusové body za chybné informace. Například, když nakreslíš schéma špatně, tak ti to prý může pokazit výsledek (říká to prý Sysel u ústní).

Prý chodí a kontroluje, takže taháček se prý nedá použít. Ale na druhou stranu to jeden borec opsal celé z hodinek.

Témata se na raních termínech a odpoledních mohou lišit.

Někdo napsal, že před ústní na chodně se můžeš podívat na mobil a zkusit si rychle ještě dané téma zopakovat.

Prý Syslovi záleží na principech fungování komponent, obrázky a schémata, že prostě vidí, že rozumíš tomu, jak to funguje. Neučená čísla, přenosové rychlosti a letopočty už pro něj nejsou tak podstatná.

## Nejčastejší témata

| Téma                                | Podtéma                                                          | Zmíněno na DC        |
|-------------------------------------|------------------------------------------------------------------|----------------------|
| Procesor                            |                                                                  | 34                   |
|                                     | schéma                                                           | 11                   |
|                                     | skalarita                                                        | 2                    |
|                                     | superskalarita                                                   | 12                   |
|                                     | postup zpracování - PF, D1, D2, EX, WB                           | 1                    |
|                                     | k čemu je Z-buffer                                               | 1                    |
|                                     | pipeline                                                         | 5                    |
|                                     | informační kanál                                                 | 1                    |
|                                     | princip                                                          | 2                    |
|                                     | instrukční kanály                                                | 1                    |
| Polovodičové paměti                 |                                                                  | 10                   |
|                                     | jak fungují                                                      | 1                    |
|                                     | rozdělení/úrovně                                                 | 2                    |
|                                     | kde se nachází                                                   | 1                    |
|                                     | jednu vybrat a popsat podrobně                                   | 1                    |
| Paměti obecně                       |                                                                  | Součet RAM + HHD/SSD |
|                                     | Hierarchie                                                       | 1                    |
| Grafická karta                      |                                                                  | 23                   |
|                                     | schema                                                           | 2                    |
|                                     | části                                                            | 8                    |
|                                     | pipeline (jen popis bez obrázku)                                 | 12                   |
|                                     | jak funguje 3D (pipeline)                                        | 5                    |
|                                     | dac, atd...                                                      | 1                    |
|                                     | jak se vytváří obraz                                             | 1                    |
|                                     | grafické sub systémy                                             | 3                    |
| Základní deska                      |                                                                  | 17                   |
|                                     | schéma                                                           | 6                    |
|                                     | bios/uefi                                                        | 6                    |
|                                     | co na ní patří                                                   | 1                    |
| Sběrnice                            |                                                                  | 12                   |
|                                     | jak dělíme (rozdělení/typy)                                      | 5                    |
|                                     | jednu vybrat a popsat                                            | 5                    |
|                                     | popsat fungování                                                 | 1                    |
|                                     | typy přenosu                                                     | 1                    |
|                                     | prý hlavně PCI-e                                                 | 1                    |
| Tiskárny                            |                                                                  | 4                    |
|                                     | 3 nejpoužívanější podrobně popsat (2x inkoustová, laserová, led) | 4                    |
|                                     | Barvy CMYK a RGB                                                 | 1                    |
|                                     | Bývá jako doplňující otázka                                      | 1                    |
| USB sběrnice                        |                                                                  | 10                   |
|                                     | Architektura                                                     | 1                    |
|                                     | Typy komunikace                                                  | 1                    |
|                                     | Konektory                                                        | 1                    |
|                                     | Vrstvy                                                           | 1                    |
|                                     | Typy přenosu                                                     | 1                    |
| Sekudární uložné zařízeni (HDD/SSD) |                                                                  | 8                    |
|                                     | komplet jak funguje hdd/ssd                                      | 1                    |
|                                     | jednotlivé části                                                 | 1                    |
|                                     | úrovně                                                           | 1                    |
| LCD display (doplňující)            |                                                                  | 2                    |
| Optická média (doplňující)          |                                                                  | 1                    |
| Co je mikrooperace (doplňující)     |                                                                  | 1                    |
| Plugun and Play (doplňující)        |                                                                  | 1                    |

## Témata seřazená podle pravděpodobnosti

1. Procesor (28,8%)
2. Grafická karta (19,5 %)
3. Paměti obecně (15,2 %)
   1. Polovodičové paměti (8,5 %)
   2. Sekundární uložiště (6,8 %)
4. Základní deska (14,4 %)
5. Sběrnice (10,2 %) 
7. USB sběrnice (8,5 %)
8. Tiskárny (3,4 %)
9. LCD display - doplňující
10. Opatická média - doplňující
11. Co je mikrooperace - doplňující
12. Plug and Play - doplňující

# CPU

Toto schéma chce znát:
![Základní CPU Schéma](./image0.jpg)

![CPU co chce dle lidí](./Screenshot%202026-05-16%20at%208.17.40.png)

# GPU

![GPU pipeline](./Screenshot%202026-05-16%20at%208.18.58.png)

# USB

![USB DC](./Screenshot%202026-05-16%20at%208.22.41.png)