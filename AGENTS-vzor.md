---
nazev: AGENTS.md, návod pro AI i pro lidi
vlastnik: <jméno a příjmení>
oblast: pravidla
zdroj: vzorová verze
plati_do: <RRRR-MM-DD, rok od poslední revize>
stav: navrh
posledni_zmena: <RRRR-MM-DD (kdo)>
---

# AGENTS.md – návod pro AI i lidi (čti jako první)

**Vzor, verze 1.0** | listopad 2026 | Adam Le Hanka, trpAIzlíci s.r.o.

> **Pro člověka, který vzor zavádí. AI tenhle blok ignoruje; po úpravě ho smažte i s řádkem nad ním.**
>
> - Je to obecná verze souboru. Nepočítá s žádným oborem ani nástrojem, hodí se na jakoukoli složku, do které se sbírají podklady a ze které vzniká práce: projekt, agenda útvaru, znalostní báze, osobní poznámky.
> - Všechno v `<špičatých závorkách>` nahraďte vlastními údaji. Co se vás netýká, smažte. Nejdůležitější je sekce 1: bez ní AI neví, k čemu složka slouží.
> - Soubor přejmenujte na `AGENTS.md` a dejte ho do kořene složky (knihovna v SharePointu, sdílená složka, repozitář).
> - Claude Code, Cursor nebo GitHub Copilot si soubor s tímhle názvem načtou samy. V Microsoft 365 Copilotu se sám nenačte: text vložte do instrukcí agenta, nebo soubor přidejte agentovi mezi zdroje a v instrukcích na něj odkažte. Co z toho u vás funguje líp, je potřeba vyzkoušet.
> - Držte ho krátký. Pravidlo sem patří, když platí pro všechny, kdo se složkou pracují, a když by ho potřeboval nový kolega první den.
> - Po první úpravě přepněte v hlavičce `stav` na `platne` a doplňte vlastníka a datum revize.

## 1. K čemu tahle složka je

- **Účel:** `<jednou až třemi větami: co se tu dělá a pro koho>`
- **Kdo s ní pracuje:** `<tým, role nebo jména>`
- **Co se tu sleduje:** `<věci, které mají svůj stav a historii, např. projekty, dodavatelé, produkty, případy, žádosti>`. Dál se jim tu říká **témata**.
- **Co je hotová práce:** `<jaké výstupy odsud odcházejí a komu>`
- **Co sem nepatří:** `<co se řeší jinde a kde>`

## 2. Struktura složky

```
<nazev-slozky>/
├── AGENTS.md            # tenhle návod
├── 00_podklady/         # suroviny, jak přišly. Jen se přidává
├── 10_znalosti/         # co platí dlouhodobě
├── 20_aktualni_stav/    # co platí teď: karty témat, todo.md, cekame-na.md
├── 30_vystupy/          # co odsud odchází
├── _archiv/             # hotové úkoly a zastaralé soubory, nic se nemaže
└── zpracovano.md        # který podklad je zpracovaný a kam se propsal
```

| Kde | Co tam patří |
|---|---|
| `00_podklady/<druh>/` | Podklady roztříděné podle druhu: `<např. maily, zápisy, dokumenty, poznámky>`. Jeden podklad = jeden soubor. |
| `10_znalosti/rozhodnuti.md` | Co platí, kdo to rozhodl, kdy a odkud to víme. |
| `10_znalosti/<nazev>.md` | Znalosti podle témat, ne podle podkladů: `<např. slovník pojmů, postupy, definice, šablony>`. |
| `20_aktualni_stav/karty/<tema>.md` | Karta tématu: aktuální stav, lidé, rizika a rozpory, historie. |
| `20_aktualni_stav/todo.md` | Co máme udělat my. Jen otevřené úkoly. |
| `20_aktualni_stav/cekame-na.md` | Na co čekáme od druhých. Jen otevřené položky. |
| `30_vystupy/` | Texty a soubory, které připravujeme nebo jsme odevzdali. |
| `_archiv/archiv-ukolu.md` | Hotové a zahozené úkoly a vyřízená čekání. |
| `_archiv/` | Soubory, které přestaly platit: nahrazené verze výstupů, karty uzavřených témat. |

Tok práce: nový podklad → `00_podklady` → zpracování do `10_znalosti` a `20_aktualni_stav` → řádek v `zpracovano.md` → z platného stavu vznikají `30_vystupy`.

### Pojmenování

- Podklady: `RRRR-MM-DD_tema_kratky-popis.md`, malá písmena, bez diakritiky, slova oddělená spojovníkem.
- Výstupy: `tema_co-to-je-vN.md`. Nová verze je nový soubor (`-v2`), starou nepřepisuj.

## 3. Základní pravidla

1. **Podklady se nemění.** Do `00_podklady` se jen přidává: žádné přepisování, opravy překlepů ani mazání. Výklad a souvislosti patří do karet a do rozhodnutí.
2. **Každý fakt má zdroj:** název podkladu bez přípony ve zpětných apostrofech, např. `2026-10-01_tema_kratky-popis`. Odkaz musí vést na existující soubor v `00_podklady`. Bez zdroje nic nezapisuj.
3. **Podklad se zpracuje celý** (dlouhé soubory čti po částech) a nakonec dostane řádek v `zpracovano.md`.
4. **Změny neztrácej.** Starou hodnotu přeškrtni a připiš novou se zdrojem: ~~3. 12.~~ → 10. 12. (`zdroj`). Nahrazené rozhodnutí nemaž, označ ho NAHRAZENO a odkaž na nové.
5. **Rozhodnutí má vždy čtyři věci:** co platí, kdo rozhodl, kdy, zdroj. Co ještě nikdo neodsouhlasil, je NÁVRH, ne rozhodnutí.
6. **Sliby a žádosti.** Náš slib („pošlu“, „dodáme“) je úkol v `todo.md`. Naše žádost na někoho jiného je položka v `cekame-na.md`. Otázka, na kterou jsme neodpověděli, je úkol v `todo.md`.
7. **Termíny porovnávej s dnešním datem.** Úkol po termínu dostane ❗ PO TERMÍNU. Čekání delší než `<14 dní>` bez reakce potřebuje úkol na urgenci.
8. **Co nevíš, nedomýšlej.** Chybějící údaj, otázku bez odpovědi nebo rozpor, který nikdo nerozhodl, zapiš do `todo.md` jako `- [ ] MEZERA: … – téma – zdroj`.
9. **Jazyk:** `<česky; výjimky, např. s kým a kdy anglicky>`

## 4. Archivování

V `todo.md` a `cekame-na.md` je jen to, co je otevřené. Vyřízené věci se přesouvají do archivu, aby pracovní soubory zůstaly krátké a historie se neztratila.

1. **Hotový nebo zahozený úkol** v tomtéž kroku smaž z `todo.md` a připiš do `_archiv/archiv-ukolu.md`. Nenechávej ho v `todo.md` odškrtnutý ani přeškrtnutý.
2. **Vyřízené čekání** (odpověď přišla, nebo už na ni nečekáme) přesuň z `cekame-na.md` stejným způsobem.
3. **Zápis v archivu** říká, jak to dopadlo a kde je výsledek. U zahozeného úkolu napiš „zahozeno“ a krátce proč. Řadí se po měsících, nejnovější nahoře.
4. **Soubor, který přestal platit** (nahrazená verze výstupu, karta uzavřeného tématu, znalost, která už neplatí), přesuň do `_archiv/` a v hlavičce mu nastav `stav: zastarale`.
5. **Z archivu se nic nemaže a nic se v něm nepřepisuje.** Jako zdroj platného stavu se nepoužívá: když archiv odporuje kartě nebo rozhodnutí, platí karta a rozhodnutí.
6. **Podklady se nearchivují.** Zůstávají v `00_podklady`, i když je téma uzavřené.

## 5. Hlavička souboru

Každý soubor v `10_znalosti`, `20_aktualni_stav` a `30_vystupy` má hlavičku. Podklady ji nemají, protože se nemění. Při práci porovnej `plati_do` s dnešním datem: soubor s prošlou platností nebo se stavem `zastarale` neber jako platný zdroj a ve výstupu to řekni.

```
---
nazev: <název, jak by ho řekl člověk>
vlastnik: <jméno>
oblast: <oblast>
zdroj: `<podklad-1>`, `<podklad-2>`
plati_do: <RRRR-MM-DD>
stav: platne
posledni_zmena: <RRRR-MM-DD (kdo)>
---
```

| Pole | Co tam patří |
|---|---|
| `nazev` | Název souboru, jak by ho řekl člověk. |
| `vlastnik` | Kdo rozhoduje, co v souboru platí. |
| `oblast` | Jedna z vašich oblastí: `<seznam, např. rozhodnuti, karty, provoz, vystup, pravidla>` |
| `zdroj` | Hlavní podklady. U karet a rozhodnutí stačí „u jednotlivých faktů“. |
| `plati_do` | Kdy soubor znovu zkontrolovat. Karty, `todo.md` a `cekame-na.md`: `<3 měsíce>` od poslední změny. Rozhodnutí a pravidla: `<12 měsíců>`. Výstup: do odevzdání. |
| `stav` | `navrh`, `platne` nebo `zastarale`. Soubory v `30_vystupy` zakládá AI jako `navrh`, na `platne` je přepne až člověk. |
| `posledni_zmena` | Datum a kdo. Přepiš při každé úpravě. |

Soubor bez hlavičky: doplň ji při nejbližší úpravě a zapiš to do `zpracovano.md`. V SharePointu se dají stejná pole vést i jako sloupce knihovny.

## 6. Akce mimo složku

`<Smažte, pokud AI u vás nesahá do pošty, kalendáře ani jiných systémů.>`

1. **Nic neodchází bez člověka.** Mail jen jako koncept, zápis do jiného systému jen jako návrh. Odeslat nebo potvrdit až tehdy, když to člověk výslovně řekne.
2. **Kalendář:** nová událost má v názvu `[REZERVACE]`, dokud ji druhá strana nepotvrdí. Před vytvořením zkontroluj kolize. Kolizní termín nevytvářej, navrhni jiný.
3. **Každá akce mimo složku má stopu ve složce:** koncept nebo událost je řádek v `todo.md` nebo `cekame-na.md` (co, kde to je, zdroj).
4. **Údaj, který nenajdeš, si nevymýšlej** (adresa, číslo, jméno). Nech ho prázdný a do `todo.md` zapiš, co je potřeba doplnit.

## 7. Formáty řádků

- todo: `- [ ] úkol – téma – zdroj – termín`
- čekáme na: `- co – od koho – od kdy – zdroj – stav`
- zpracováno: řádek tabulky `| podklad | téma | zpracováno | propsáno do |`
- archiv: `- datum – úkol nebo čekání – téma – jak to dopadlo, kde je výsledek`

## Změny

- `<RRRR-MM-DD – kdo – co – proč>`
