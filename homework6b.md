# Domácí úloha č. 6

Termín: skupina 07/08: **23. 12. 23.59.59** (specialita: napište mi jakmile budete chtít úlohu opravit)

Odevzdání: Odevzdávarna v ISu odevzdávejte právě jeden soubor **.py**!

Dotazy: jan.drabek@mail.muni.cz

### Zadání

#### 1. úkol: Práce s obrázky

Napište funkci ``stripe_images(path1, path2, size=50)``, která vezme **cestu** ke dvěma obrázkům a vytvoří (a zobrazí) obrázek třetí o rozměrech průniku obou obrázků a postupně střídá pruhy z prvního a druhého obrázku o šířce ``size``.  

*V případě, že jsou obrázky rozměry obrázků liší, vezme se jen společná část.*

*Můžete předpokládat, že obrázky existují. Na velkých obrázcích může   provedení trvat přes minutu.*

Bonus (2 body): přidejte parametr ``chessboard`` typu ``Bool``, při jehož aktivací dojde k vytvoření šachnovice polí ``size``x``size`` z jednotlivých obrázků nastřídačku.

![Ukázka včelí plástve](data/example-stripes.png)

#### 2. Vánoční cenzura

Motivace: mnoho textů nemá patřičnou vánoční atmosféru a to je na čase změnit!

Napište třídu `Censor`, která bude mít následující metody:

- konstruktor, který bude příjímat jeden nepovinný argument `case_insensitive`, který bude řídit, zda při porovnávání záleží na velikosti. Výchozí hodnota je `False`.
- `add_replacement(needle, replacement)`, která způsobí, že tento cenzor při budoucích cenzurách nahradí `needle` za `replacement`
- `add_censoring(needle, char, leave_start = False)`, která způsobí, že tento cenzor při budoucích cenzurách přepíše každý znak `needle` za `char` (vždy délky 1). V případě, že `leave_start` je True, ponechá se první znak tohoto slova.
- `toogle_statistics()`, která změní stav zobrazování statistik (výchozí stav je nezobrazování), pokud se mají statistiky zobrazovat, pak po skončení každé cenzury funkcí `censor` (viz dále) vytiskne na standardní výstup statistiku kolik slov, bylo kterým způsobem cenzurováno.
- `censor(input_path, output_path)`, která bere cestu ze které načte textový soubor a druhou cestu do které uloží cezurovaný soubor, podle nastavených pravidel.
- (Bonus za 2 body) `add_regex_replacement(pattern, replacement)`, která způsobí, že tento cenzor při budoucích cenzurách každý `pattern` (vyhodnocovaný po slovech) nahradí za `replacement` (vhodná funkce `re.sub` či `re.subn`).

Následně použijte vámi naimplementovanou třídu k dosažení vánoční ~~cenzury~~ atmosféry na souboru:

- Vyberte si soubor a odkaz na něj dejte jako komentář v souboru.
- Vytvořte cenzora a nastavte ho tak, aby v souboru vytvořil tu správnou vánoční atmosféru (používajíc přitom všechny naprogramované funkce).

Důležité poznámky:

- Pořadí vyhodnocování cenzur je: nahrazení, regexové nahrazení, cenzurování.
- Doporučuji číst soubor po řádcích a vyhodnocovat po slovech (řádkování musí zůstat zachováno, nicméně bílé místo mezi slovy může být normalizováno na mezery.
- Můžete předpokládat, že slova jsou oddělena prázdným místem.
- Pokud už cenzura pro daný typ a slovo existuje, přepište jej a vypište o tom hlášku na standardní výstup.
- Najděte si vhodný text, například http://www.gutenberg.org/files/13083/13083-0.txt se může hodit.