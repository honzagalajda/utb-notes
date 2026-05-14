# Základní výpočty

## Převody bajtů a bitů

1 bajt (B) = 8 bitů (b)
### Příklady:
<details>
<summary>Textový soubor "data.txt" má velikost 137 bajtů. Jaká je velikost
tohoto souboru v bitech ?</summary>

$$
137 \times 8 = 1096
$$
</details>
<details>
<summary>Jak dlouho potrvá přenos 100 000 bitů při rychlosti 1200 bitů/s?</summary>

$$
s = v \times t
$$
$$
t = \frac{s}{v}
$$
$$
t = \frac{100 000}{1 200} = 83,33
$$
</details>

## Aritmetický a Vážený průměr:

### Příklad:

<details>
<summary>Určete aritmetický a vážený průměr pro předměty ve formátu P(známka, váha): P1(1, 8), P2(2, 4), P3(2, 3), P4(3, 1), P5(2, 2).</summary>

**Aritmetický průměr:**

$$
⌀ = \frac{1 + 2 + 2 + 3 + 2}{5} = 2
$$

**Vážený průměr:**

$$
⌀ = \frac{(1 \times 8) + (2 \times 4) + (2 \times 3) + (3 \times 1) + (2 \times 2)}{8 + 4 + 3 + 1 + 2} = 2
$$

</details>

## Logaritmy

$$
y = log_ax => a^y = x
$$

$$
log_ax = \frac{log_bx}{log_ba}
$$

# Kombinatorika

A zároveň = násobení

Nebo = sčítání

![Screenshot 2026-05-12 at 15.46.41.png](./Screenshot%202026-05-12%20at%2015.46.41.png)

$n$ = celkový počet prvků, ze kterých můžeme vybírat

$k$ = počet prvků, které vybíráme

## Variace bez opakování

$$
V(k, n) = \frac{n!}{(n-k)!}
$$

Používáme, když nám **záleží na pořadí** prvků a prvky se **nemohou opakovat**.

### Příklad:

<details>
<summary>
Jsou dány cifry 1, 2, 3, 4, 5. Cifry nelze opakovat. Kolik z těchto cifer můžeme sestavit dvojmístných a trojmístných čísel?
</summary>

$$
V(2, 5) + V(3, 5) = 20 + 60
$$

</details>

## Variace s opakováním

$$
V'(k, n) = n^k
$$

Používáme, když nám **záleží na pořadí** prvků a prvky se **mohou opakovat**.

### Příklad:

<details>
<summary>
Kolik různých hodů lze provést pomocí zadaného počtu různobarevných
(šestistěn.) kostek. a) Dvě různobarevné kostky? b) Tři různobarevné kostky? c) Pět různobarevných kostek.
</summary>

**A)**
$$
n = 6
$$
$$
k = 2
$$
$$
6^2 = 36
$$

**B)**
$$
n = 6
$$
$$
k = 3
$$
$$
6^3 = 216
$$

**C)**
$$
n = 6
$$
$$
k = 3
$$
$$
6^5 =7776 
$$
</details>

## Permutace bez opakování

$$
P(n) = n!
$$

Používáme, když nám **záleží na pořadí**, prvky se **nemohou opakovat** a **$k = n$**.

### Příklady:

<details>
<summary>
Jsou dány cifry 1, 2, 3, 4, 5. Cifry nelze opakovat. Kolik z těchto cifer je možno vytvořit pětimístných sudých čísel?
</summary>

$$
\_\space\_\space\_\space\_\space2
$$
$$
\_\space\_\space\_\space\_\space4
$$

Na volná místa (_) můžeme dosadit $4!$ číslic (nejprve 4, potom 3, potom 2 a nakonec už jen jednu). Na posledním místě budou vždy jen číslice 2 nebo 4, abychom zajistili, že výsledné číslo bude sudé. Tzn.

$$
4! \times 2 = 24 \times 2 = 48
$$

</details>

<details>
<summary>
Jsou dány cifry 1, 2, 3, 4, 5. Cifry nelze opakovat. Kolik z těchto cifer je možno vytvořit pětimístných čísel končících dvojčíslím 21?
</summary>

$$
\_\space\_\space\_\space2\space1
$$

Na zbývající 3 pozice lze dosadit 3 čísla (3, 4, 5), což znamená, že můžeme dosadit $3!$ (nejprve 3 čísla, potom 2 a potom už jen poslední). Tzn.

$$
3! = 6
$$
</details>

## Permutace s opakováním

$$
P'(n_1, n_2... n_m) = \frac{n!}{n_1! \cdot n_2! \cdot ... \cdot n_m!}
$$

Používáme, když nám **záleží na pořadí**, prvky se **mohou opakovat** a **$k = n$**.

## Kombinace bez opakování

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

Používáme, když nám **nezáleží na pořadí** a prvky se **nemohou opakovat**.

### Příklad:

<details>
<summary>
Na setkání po 10 letech si účastníci cinkli sklenicemi. Uskutečnilo se 45
cinknutí. Kolik účastníků se setkání zúčastnilo?
</summary>

$$
celkem = 45
$$
$$
k = 2
$$
$$
n = ?
$$
$$
\frac{n!}{2!(n-2)!} = 45
$$
$$
\frac{n\times(n-1)\times(n-2)!}{2(n-2)!} = 45
$$
$$
\frac{n\times(n-1)}{2} = 45 \space/\times2
$$
$$
n^2-n-90 = 0
$$
$$
D = 1+360 = 361
$$
$$
\sqrt{D} = 19
$$
$$
n_1 = \frac{1+19}{2} = 10
$$
$$
n_2 = \frac{1-19}{2} = -9
$$
</details>

## Kombinace s opakováním

$$
C'(k, n) = \binom{n + k - 1}{k}
$$

Používáme, když nám **nezáleží na pořadí** a prvky se **mohou opakovat**.

# Pravděpodobnost

$$
P = \frac{m}{n}
$$

$m$ = chtěný počet prvků

$n$ = celkový počet prvků

Podmíněná pravděpodobnost znamená, že se celkový počet možností zúží na ty případy, kdy je daná podmínka splněna.

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

# Převody

## Binární soustava

`0, 1`

### Sčítání

Funguje na základě posouvání zbytku (1) do dalšího sloupce.

$$
1111\\\\\space\space\space01011\\\frac{+01111}{\space\space\space11010}
$$

### Odčítání

Funguje na základě půjčování si dvojky neboli 2 z následujícího sloupce.

$$
\space\space\space01011\\\ -01111
$$

Musím to nejprve otočit:

$$
\space\space\space01111\\\frac{-01011}{\space\space\space-100}
$$

### Násobení

Funguje stejně jako normální násobení. Nejprve spodní čísla postupně násobím každým vrchním číslem, kdy u 0 píšeme vždy 0 a u 1 řádek opisujeme. Potom všechna čísla sečteme.

### Dělení 

Funguje jako dělení polynomu polynomem. Když zjišťuješ, jestli by se jedno číslo do druhého vešlo, podle toho napíšeš 1 nebo 0 a pokračuješ dál, dokud to už nejde.

## BCD kód

Převádím každou desítkovou číslici zvlášť do binárního kódu. Tzn.

$$
78 = 0111\space1000
$$

## Římské číslice

$I = 1$

$V = 5$ (nelze použít pro odečítání)

$X = 10$

$L = 50$ (nelze použít pro odečítání)

$C = 100$

$D = 500$ (nelze použít pro odečítání)

$M = 1000$

## Osmičková soustava

`0, 1, 2, 3, 4, 5, 6, 7`

<details>
<summary>
Převeď číslo 49 z desítkové do osmičkové soustavy
</summary>

$$
49:8 = 6\space zb.1
$$
$$
6:8 = 0\space zb.6
$$
$$
49 = 61
$$
</details>

### Sčítání, odčítání a násobení

Funguje stejně jako v desítkové, jenom neustále uvažujeme, že maximální číslo, které můžeme zapsat, je 7. Podle toho pak určujeme, kolik jde dál. Když nám vyjde, že součet je 10, tak 1 nám jde dál a 2 (10 - 8) zapíšeme.

## Hexadecimální (šestnáctková) soustava

`0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F`

<details>
<summary>
Převeď číslo 49 z desítkové do hexadecimální soustavy
</summary>

$$
49:16 = 3\space zb.1
$$
$$
3:16 = 0\space zb.3
$$
$$
49 = 31
$$
</details>

### Sčítání, odčítání a násobení

Funguje úplně stejně jako v desítkové.

## Big Endian vs Little Endian

Big: `12 34 56 78`

Little: `78 56 34 12`

## IEEE 754

![IEEE 754](./Screenshot%202026-05-13%20at%2022.02.38.png)

Sign = 1 = záporné číslo; 0 = kladné číslo

Exponent = základem je 127; přičítáme k tomu, kolikrát jsme doleva posunuli desetinnou čárku, abychom dostali číslo 1,.....

Mantisa = zde zapíšeme zbytek za desetinou čárkou.

Dá se také zapsat jako 4 dvojice hex čísla. Jako příklady endianness jsou v tomto souboru například.

### Sčítání

[Tady je to hezky vysvětleno](https://numeral-systems.com/ieee-754-add/)

### Odčítání

[Dole je vysvětlené i odčítání](https://numeral-systems.com/ieee-754-add/)

### Násobení

[Tady je to hezky vysvětlené](https://numeral-systems.com/ieee-754-multiply/). Rozdíl oproti sčítání nebo odčítání je ten, že exponenty se sečtou a odečte se od nich bias (127), čímž získáme finální exponent. Mantisy mezi sebou roznásobíme, tak jak jsou. A desetinná čárka se po násobení dává podle součtu číslic za desetinou čárkou obou číslic.

### Dělení

[Tady je to hezky vysvětlené](https://numeral-systems.com/ieee-754-divide/). Při dělení se jen pozor na to, že exponenty se od sebe odečítají a bias se přičítá!

---

**Poznámky při učení:**
- Dokument 3 mi zatím dělal největší problém (projeď s Vojtou) prostě **pravděpodobnost**