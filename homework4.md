# Domácí úloha č. 4

Termín: 

- skupina 07: 19. 11. 23.59.59
- skupina 08: 19. 11. 23.59.59

Odevzdání: Odevzdávarna v ISu odevzdávejte ideálně jeden soubor **.py**, nikdy ne archiv! V případě více souborů je nahrajte postupně všechny.

Dotazy: jan.drabek@mail.muni.cz

Vytvořte program hrající hru "Jednorozměrné piškvorky" proti uživateli (na plánu zadané velikosti). Tato variace piškvorek se hraje na jednorozměrném hracím plánu, tj. hrací  plán je řada čtverečkovaných políček. Stejně jako u běžných piškvorek se  hráči střídají a dělají značky do políček, tentokrát však oba hráči dělají  hvězdičky. Vyhrává hráč, který jako první vytvoří alespoň tři hvězdičky vedle sebe.

### Zadání

Vaším úkolem je implementovat:

* Funkci `strategy(state)`, která pro daný plán vrátí pozici optimálního tahu. Plán je reprezentován polem znaků `*` (hvězdička reprezentované znakem *) a `_` (neobsazené
  pole).

```
>>> state = ['_', '_', '_', '*', '*', '_', '_', '*']
>>> strategy(state)
2
```

* Funkci `tictactoe(size, human_starts=True)`, která umožňuje hrát hru jednorozměrných piškvorek s počítačem. Můžete předpokládat, že zadaná velikost plánu je rozumná (alespoň 3 a méně než 50). Parametr `human_starts` určuje, zda začíná hráč nebo počítač. Výpis průběhu hry má být stejný, jako v následujících příkladech (= bude penalizace pokud nebude). Funkce kontroluje, zda jsou tahy zadané hráčem platné a pokud nejsou, vyzve ho k novému zadání. Pro tahy počítače volejte výše uvedenou funkci `strategy(state)`.

### Příklady hry

Příklad, v němž začíná hráč:

    >>> tictactoe(26, human_starts=True)
    _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _
    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5
             0         |         1         |     2

    Na tahu: hrac
    Zadej tah: 1

    _ * _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _
    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5
             0         |         1         |     2

    Na tahu: pocitac
    Zahral na pozici: 4

    _ * _ _ * _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _
    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5
             0         |         1         |     2

    Na tahu: hrac
    Zadej tah: 6

    _ * _ _ * _ * _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _
    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5
             0         |         1         |     2

    Na tahu: pocitac
    Zahral na pozici: 5

    _ * _ _ * * * _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _
    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5
             0         |         1         |     2

    Prohrál jsi!


### Bodování

Funkce `tictactoe(size, human_starts=True)` musí korektně provádět
hru hráče a počítače, kontrolovat zadané tahy hráče a určit výhru. Výpis se musí shodovat s výše uvedenými ukázkami, takže obě funkce musí mít stejnou signaturu (jméno, parametry)

Základní variantou `strategy` je funkce, která dodržuje pravidla, ale jinak hraje náhodně. Za takové řešení obdržíte až 22 bodů (při splnění všech požadavků na funkci `tictactoe()`). Abyste získali 25 bodů, musí program hrát alespoň trochu rozumně, např. když může jedním tahem vyhrát, tak to udělá, a nenahrává na výhru, pokud se tomu lze vyhnout, vyhrává na plánech liché délky když začíná...
Pokud váš program bude hrát "inteligentně", získáte bonusové
body. Čím inteligentněji, tím více bodů.

V každém případě napište do komentáře stručné vysvětlení, jak moc inteligentně program hraje a proč. Kvalita tohoto popisu je také důležitá.

### Několik tipů

*  Než začnete psát kód, rozmyslete si (nejlépe si i nakreslete) dekompozici problému na jednodušší funkce. Jinak se v tom ztratíte. Problém lze rozložit různě, příklady užitečných funkcí: `show_state(state)`, `is_won(state)`, `valid_move(move, state)`, ale v průběhu řešení by vás pak měly napadnout ještě další. Kdykoliv zjistíte, že máte v programu duplicitní kód, zbavte se ho (např. právě pomocí nové pomocné funkce). A všechny funkce by měly zůstat dostatečně krátké a přehledné.
* Začněte variantou s náhodnými tahy, rozumné chování přidejte až potom. Při dobré dekompozici by rozšiřování neměl být problém.
* Zkuste si tuto hru párkrát zahrát (s někým nebo i sami se sebou), pomůže vám to lépe pochopit, jak by měl počítač optimálně hrát.

### Důležité poznámky

* Odevzdejte pouze jediný soubor `uloha04.py`, s definicemi funkcí `strategy(state)` a `tictactoe(size, human_starts=True)` (a dalšími pomocnými funkcemi dle vaší dekompozice). Dodržte tyto názvy funkcí a parametrů (kvůli částečně automatickému opravování úlohy).
* Nepoužívejte diakritiku (ani v komentářích).
* Pro jistotu ještě jednou: dodržte kostru programu i výpis průběhu hry tak, jak je uvedené v zadání.
