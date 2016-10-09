# Domácí úloha č. 2

Termín: 

- Skupina 07: 22. 10. 23.59.59
- Skupina 08: 22. 10. 23.59.59

Odevzdání: Odevzdávarna v ISu odevzdávejte právě jeden soubor **.py**, nikdy ne archiv!

Dotazy: **výhradně** jan.drabek@mail.muni.cz

## Zadání

**Zákeřné rozdělování sladkostí**

Motivace: máme `n` sladkostí a potřebujeme je rozdělit mezi `m` dětí. A protože nechceme být tak úplně hodní, rozhodli jsme se použít čtyřstěnnou kostku, kterou si děti postupně hází a dle součtu hodů dostávají sladkosti (přesná pravidla níže).

**Úkol 1: Vytvořte simulátor zákeřného rozdělování sladkostí**

Pravidla:

- Ve hře je `n` sladkostí a `m` dětí (pojmenované 1 až `m`).
- Začíná dítě se jménem 1.
- Každé dítě háže kostkou (`1`-`4`), když padne `4`, hází se znovu.
- Každé dítě získá buď tolik sladkostí kolik je součet jeho hodů, nebo nic v případě, že je součet větší než počet zbývajících sladkostí.
- Hra končí když dojdou sladkosti.

Poznámky:

- Při počtu sladkostí `< 1` či počtu dětí `< 1` skončete funkci a vypište nějakou smysluplnou hlášku.
- V případě, že každé dítě už házelo, jede se znovu od prvního dítěte.


Ukázkový výpis programu:

```
>>> game (40, 3)
1. dite: 3 -> Dostane: 3 -> Zbyva sladkosti: 37
2. dite: 3 -> Dostane: 3 -> Zbyva sladkosti: 34
3. dite: 3 -> Dostane: 3 -> Zbyva sladkosti: 31
1. dite: 2 -> Dostane: 2 -> Zbyva sladkosti: 29
2. dite: 2 -> Dostane: 2 -> Zbyva sladkosti: 27
3. dite: 3 -> Dostane: 3 -> Zbyva sladkosti: 24
1. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 23
2. dite: 2 -> Dostane: 2 -> Zbyva sladkosti: 21
3. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 20
1. dite: 2 -> Dostane: 2 -> Zbyva sladkosti: 18
2. dite: 4 1 -> Dostane: 5 -> Zbyva sladkosti: 13
3. dite: 4 1 -> Dostane: 5 -> Zbyva sladkosti: 8
1. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 7
2. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 6
3. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 5
1. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 4
2. dite: 1 -> Dostane: 1 -> Zbyva sladkosti: 3
3. dite: 3 -> Dostane: 3 -> Zbyva sladkosti: 0
Rozdelovani dokonceno v 18. kole
```

**Úkol 2: Vytvořte funkci, který analyzuje kolik průměrně tahů (vrátí typ float) rozdělování je potřeba pro zadaný počet sladkostí, počet dětí a počet opakování.**

**Úkol 3: Pomocí funkce z úkolu 2 zjistěte průměrné počty kol rozdělování pro počty sladkostí 1-50 pro variabilní počet dětí (viz parametr `children` u funkce `game_average_length`).**

## Kostra

```
from random import randint, randint

def game(sweets, children, output = True):
    pass

def game_analysis(sweets, children, count):
    pass

def game_average_length(children, count):
    pass
```
