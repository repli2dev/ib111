# Domácí úloha č. 5

Termín:

- skupina 07: 10. 12. 23.59.59
- skupina 08: 10. 12. 23.59.59

Odevzdání: Odevzdávarna v ISu odevzdávejte právě jeden soubor **.py**!

Dotazy: jan.drabek@mail.muni.cz

### Zadání

Vytvořte jednoduchou simulaci světa, ve kterém se pohybují myši a kočky:

- Svět má podobu M x N mřížky (M i N se zadávají při vytváření světa).
- Na náhodných políčkách jsou neprůchodné překážky (jejich pozice je generována náhodně dle pravděpodobnosti zadané při vytváření světa).
- Myš/kočka zabírá jedno políčko a začíná na náhodném poli (pozor na překážky).
- Myš/kočka má symbol, kterým je reprezentován na plánku, pro kočku je tento symbol vygenerován náhodně z písmen A až Z. Pro myš náhodně z čísel 1 až 9.
- Myš/kočka má základní pohyby do čtyř směrů (otáčení se neřeší).
- Myš/kočka nemůže vstoupit na políčko s překážkou či jinou myší/kočkou, v takovém případě zůstává stát.
- Myš/kočka nemůže vyjet ze světa.

Myš se hýbe náhodně. Kočka směrem k cílovému poli (stačí naivně se zaseknutím na první překážce).

Implementujte honičku jako funkci `chase(cats_count)`. Do světa přidejte 1 myš a nějaké množství koček, které budou honit myš.

Implementujte historii pohybů jednotlivých myší/koček. Po skončení vypište samostatně trasu každé myši/kočky.


### Příklad výpisu stavu světa

```
_ # _ # # _ # _ _ _ 
_ # _ _ _ _ _ _ # _ 
_ _ _ _ _ _ _ _ S _ 
_ _ _ _ _ _ _ _ # _ 
2 _ # _ _ K _ _ _ # 
# _ _ _ _ # # _ _ C 
_ _ K _ _ _ _ _ # _ 
_ _ _ _ _ # _ _ _ _ 
```


### Několik tipů

 - Využívejte objekty, nepoužívejte globální proměnné.
 - Je doporučeno definovat si dvě třídy: `World` reprezentující mřížku (+ rozměry), udržující informace o "žijících" objektech, se schopností vizualizovat aktuální svět světa. Třídu `Cat`, která reprezentuje jednu kočku, obzvláště si pamatuje její pozici a svět, ve kterém se pohybuje. A obdobně třídu `Mouse` reprezentující jednu myš.
 - Pokuste se minimalizovat copy&paste kód, dbejte na úspornost kódu (v případě tříd `Mouse` a `Cat` by se vám na to mohla hodit dědičnost).
 - Úlohu dobře rozložte na dílčí problémy. Při dobré dekompozici jsou jednotlivé metody (funkce) krátké (mají jednotky řádky).
 - Pokud si nebudete vědět rady, zkuste si ji pro začátek libovolně zjednodušit, například ignorováním překážek, uvažováním 1 robota...
 - Můžete získat bonusové body za chytřejší strategii pohybu robotů, nejprve ale implementujte základní (~ naivní strategii).
 - Hodit se může magická metoda `__str__`, díky které pak lze volat print(instance) a dostávat váš výstup. 
 - Úloha je na 25 bodů.
