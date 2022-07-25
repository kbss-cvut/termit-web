---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: single-cs
# title: Tutoriál
permalink: /cs/tutorial
lang: cs
lang-ref: tutorial
header:
  image: /assets/images/tutorial-header.jpg
  caption: "Photo credit: [**Immo Wegmann**](https://unsplash.com/@macroman?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [**Unsplash**](http://unsplash.com/)"
toc: true
---

# Tutoriál

Systém TermIt je navržen pro správu pojmů a slovníků, umožňuje ke slovníkům přiřazovat dokumenty a jiné zdroje  a propojovat je. Základní tutoriál popisuje je krok za krokem následující činnosti:
* vyhledávání pojmů a procházení slovníků,
* označování výskytů pojmů a jejich definic v dokumentech,
* vytváření nových slovníků a pojmů a jejich úpravy,
* přiřazování dokumentů ke slovníku a jejich anotace.

Chystáme pokročilý tutoriál, který podrobně ukáže pokročilé možnosti systému TermIt. Také je v přípravě dokumentace popisující všechny jednotlivé prvky systému (nezávisle na konkrétní činnosti).

## Sandbox
Na stránce <a href="https://kbss.felk.cvut.cz/termit-dev/">https://kbss.felk.cvut.cz/termit-dev/</a> se nachází vývojová verze systému TermIt. Obsahuje několik slovníků naplněných pojmy, některé z nich mají přiřazené dokumenty. Nasazení je možné procházet v několika různých režimech v závislosti na uživatelských právech:
* bez uživatelského účtu -- je možné procházet všechny slovníky a všechny pojmy, není možné editovat, anotovat ani komentovat, zobrazovat dokumenty ani jiné zdroje. Funkcionalita je velice omezená, tento režim by měl sloužit veřejnosti k prohlížení slovníků a pojmů,
* s uživatelskými právy typu "Čtenář" -- uživatel jse schopen procházet slovníky, pojmy i datové zdroje. Dále vidí rozšířené vlastnosti pojmů i slovníků, může zobrazit definici pojmu v dokumentu a jednotlivé pojmy komentovat. Nemůže pojmy ani slovníky editovat a nemůže anotovat dokumenty. Tento režim slouží pro odborné uživatele, kteří se chtějí k pojmům a slovníkům vyjadřovat, ale nechtějí je přímo editovat,
* s uživatelskými právy typu "Editor" -- uživatel má plný přístup k editace všech slovníků i pojmů a může anotovat dokumenty. Tento režim je určen pro doménové experty, kteří ovládají doménu slovníku a jsou jeho hlavními tvůrci,
* s uživatelskými právy typu "Administrátor" -- tento uživatel má plný přístup ke všem slovníkům, pojmům i datovým zdrojům, navíc může vytvářet nové uživatele a přidělovat jim uživatelská práva.
Přestože se jedná o vývojovou verzi systému, nedoporučujeme dělat změny ve slovnících, které již existují. Pro experimentování si vytvořte vlastní slovník, nebo si nainstalujte vlastní instanci systému TermIt (podle návodu v <a href="/cs/install">záložce Instalace</a>).

## Základní tutoriál
Základní úkoly, tedy ty, které budou uživtaelé systému TermIt provádět po většinu času, jsou shrnuty v základním tutoriálu. Tutoriál je rozdělen do sekcí podle jednotlivých úkolů.

### Vyhledávání pojmů a procházení slovníků

Elementárním úkolem je vyhledání pojmů. Pojmem je v TermItu myšlen koncept ve specifikovaném kontextu, například "stavba" může být reprezentována dvěma pojmy, kde jeden reprezentuje stavbu jako objekt a druhý jako proces. Pojmy jsou zpravidla definovány v kontextu slovníku, například slovníku legislativního dokumentu (pojem "budova" podle katastrálního zákona) nebo konkrétní datové sady (například koncepty BIM).

Pokusme se vyhledat pojem "Lokalita" ze slovníku "Slovník Pražských stavebních předpisů 2016 - slovník".

#### Vyhledávací lišta
Nejjednodušším způsobem vyhledávání pojmů je zadat jejich název do vyhledávací lišty umístěné v horní části stránky.

{% include figure image_path="/assets/images/tutorial-cs/vyhledavaci_lista.png" alt="Vyhledávání pojmu ve vyhledávací liště" caption="Vyhledávání pojmu ve vyhledávací liště." %}

Při zadání několika znaků se pod lištou objeví seznam výsledků odpovídající vyhledávání. Výsledky obsahují název, typ (pojem, dokument, slovník...) a zdroj. Potvrzení zadání klávesou Enter zobrazí detaily vyhledávání. Kliknutím na hledaný pojem - v tomto případě ten první v seznamu - se dostaneme na detail pojmu.

#### Prohledávání slovníků

Další způsob, jak získat předhled o pojmech, je prohledáváním slovníků. V levém panelu se nachází stránka "Slovníky". Po jejím otevření se zobrazí seznam slovníků a nad nimi řádka pro filtrování. Vyhledáme "Slovník Pražských stavebních přespisů 2016 - slovník".

{% include figure image_path="/assets/images/tutorial-cs/slovníky.png" alt="Vyhledávání slovníku" caption="Vyhledávání slovníku." %}

Po kliknutí na slovník se zobrazí jeho detail. Na úvodní stránce je vedle základních informací o slovníku otevřená záložka se seznamem všech pojmů ze slovníku v hierarchické struktuře. V řádce nad nimi je možné pojmy filtrovat.

{% include figure image_path="/assets/images/tutorial-cs/pojmy_ve_slovníku.png" alt="Procházení pojmů ve slovníku" caption="Procházení pojmů ve slovníku." %}

Po kliknutí na pojem je zobrazen jeho detail.

#### Detail pojmu

Detail pojmu obsahuje základní informace o pojmu, hierarchickou strukturu ostatních pojmů ve stejném slovníku a detailní informace o pojmu v záložkách v dolní části stránky.

{% include figure image_path="/assets/images/tutorial-cs/detail_1.png" alt="Základní informace o pojmu" caption="Základní informace o pojmu." %}


### Označování výskytu pojmů a jejich definic v dokumentech

Slovníky jsou zpravidla propojeny s dokumenty, které obsahují jejich definice a výskyty. V levém panelu otevřete stránku "Slovníky" a vyhledejte slovník "Slovník Metropolitního plánu ve verzi 3.5 návrh k projednání". Po jeho otevření ve spodní části detailu otevřete záložku "Dokument".  

{% include figure image_path="/assets/images/tutorial-cs/detail_slovníku.png" alt="Detail dokumentu přiřazeného ke slovníku" caption="Detail dokumentu přiřazeného ke slovníku." %}

Mezi detailními informacemi je název a popis dokumentu a seznam přiřazených pojmů. Jedná se o pojmy, které mají v dokumentu označen výskyt. Na spodním řádku je název dokumentu s tlačítky "Obsah" a "Odstranit". Kliknutím na "Obsah" zobrazíme text samotného dokumentu.

{% include figure image_path="/assets/images/tutorial-cs/obsah_dokumentu.png" alt="Obsah dokumentu s označenýmu výskyty pojmů" caption="Obsah dokumentu s označenýmu výskyty pojmů." %}

V textu dokumentu jsou zeleně označeny výskyty pojmů, modře jejich definice. Po kliknutí na výskyt nebo definici se otevře pop-up. Zde je možné výskyt nebo definici smazat nebo upravit. Kliknutím na její název se dostanem na detail pojmu.

{% include figure image_path="/assets/images/tutorial-cs/výskyt.png" alt="Detail výskytu pojmu" caption="Detail výskytu pojmu." %}

[comment]: <> TODO: přidat označování výskytů a definic

### Vytváření nových slovníků a pojmů

V rámci tohoto úkolu vytvoříme nový slovník, přiřadíme mu dokument a vytvoříme několik pojmů.

### Vytvoření nového slovníku

V levém panelu klikněte na "Nový slovník". Na stránce vyplňte název jako "Testovací slovník [vaše jméno]" a volitelně vyplňte popis.

{% include figure image_path="/assets/images/tutorial-cs/nový_slovník.png" alt="Dialog vytvoření nového slovníku" caption="Dialog pro vytvoření nového slovníku." %}

Ke slovníku můžete rovnou při jeho vytvoření přiřadit soubor. Pro tyto účely použijeme HTML verzi katastrálního zákona ze stránky [Zákony pro lidi](https://www.zakonyprolidi.cz/print/cs/2013-256/zneni-20210101.htm?sil=1). Klikněte na stránku pravým tlačítkem myši a vyberte "Uložit stránku jako..." (může se lišit podle použitého internetového prohlížeče). V dialogu pro vytvoření nového slovníku klikněte na řádce "Soubory" na tlačítko "+ Přidat".

{% include figure image_path="/assets/images/tutorial-cs/nový_soubor.png" alt="Dialog vytvoření nového souboru" caption="Dialog pro vytvoření nového souboru." %}

Přetáhněte stažený soubor do dialogu, nebo klikněte do horní části dialogu a vyberte HTML soubor stažený ze Zákonů pro lidi. Název souboru přepiště na "soubor pro slovník [vaše jméno]". Potvrďte stisknutím tlačítka "Vytvořit". V dialogu vytvoření nového slovníku je nyní přidán Váš nový soubor. Potvrďte vytvoření nového slovníku kliknutím na tlačítko "Vytvořit". V pravé horní části stránky vyskočí několik zelených informačních oken potvrzující úsoěšné vytvoření slovníku i souboru. Po chvíli samy zmizí.

{% include figure image_path="/assets/images/tutorial-cs/slovník.png" alt="Nový slovník úspěšně vytvořen" caption="Nový slovník je úspěšně vytvořen." %}

#### Vytvoření nových pojmů

Pojmy je možné vytvářet v detailu slovníku, nebo přímo v textu souboru. V této části tutoriálu vytvoříme několik nových pojmů v detailu slovníku.

Přejděte do detailu vašeho slovníku. V záložce "Pojmy" (měla by být otevřená jako výchozí) klikněte na tlačítko "+ Nový pojem".

V nově otevřeném dialogu vyplníme následující atributy:

* název: "Parcela" -- jedná se název pojmu, který slouží zároveň i jako jednoznačné určení pojmu v rámci slovníku,
* synonyma: "katastrální parcela" -- jedná se o texty, pod kterými je pojem také označován. Slouží především k vyhledávání a anotaci. Může obsahovat také používané zkratky. Synonymum je potřeba potvrdit stisknutím tlačítka "+ Přidat",
* definice, text: "Parcela je pozemek, který je geometricky a polohově určen a označen parcelním číslem." -- jedná se o jednoznačnou definici pojmu, zpravidla určenou v dokumentu. Definice je vždy v daném kontextu a musí být právě jedna,
* definice, zdroj: "§ 2, b)" -- označuje zdroj definice pojmu formou textu.

Další pole ponecháme prázdná a stiskneme tlačítko "Vytvořit a začít nový".

{% include figure image_path="/assets/images/tutorial-cs/pojem_parcela.png" alt="Tvorba nového pojmu" caption="Tvorba nového pojmu." %}

Podobným způsobem vytvoříme pojmy "Stavební parcela", "Pozemková parcela", "Katastrální území" a "Katastrální mapa". Definice a jejich zdroje vyplňte podle svého.

V horní části dialogu můžete přidat záložku s jinou jazykovou verzí. Pro naše nasazení systému TermIt je závazným jazykem čeština.

#### Kontrola a editace pojmů

[comment]: <> možná místo chyby používat Výsledky kontroly úplnosti pojmů

Při návratu do detailu slovníku nyní vidíme v záložce "Pojmy" seznam našich pojmů. Před každým z nich je barevná tečka, která označuje úplnost detailů pojmu.

{% include figure image_path="/assets/images/tutorial-cs/validace.png" alt="Seznam nových pojmů" caption="Seznam nových pojmů." %}

Kliknutím otevřeme detail pojmu "Pozemková parcela" a ve spodní části otevřeme záložku "Kontrola".

{% include figure image_path="/assets/images/tutorial-cs/kontrola.png" alt="Chyby v úplnosti detailů pojmu" caption="Chyby v úplnosti detailů pojmu." %}

V záložce jsou uvedeny některé chyby úplnosti pojmů. Editací pojmů se pokusíme tyto chyby opravit. V pravé horní části detailu pojmu "Pozemková parcela" klikněte na tlačítko editovat. Otevře se Vám dialog shodný s tím pro tvorbu pojmu s vyplněnými hodnotami atributů.

**Pojem nemá definován obsahový typ**

Tato chyba oznamuje, že pojem nemá definován obsahový typ. Obsahovým typem je charakter pojmu a je významný pro modelování vztahů mezi jednotlivými pojmy a odvozování dalších vlastností. Rozlišujeme typy a individuály (typem je "výrobce automobilů" a individuálem "Škoda Auto") ve čtyřech kategoriích:

* objekt/typ objektu, -- nezávislé, v čase se měnící prvky,
* vlastnost/typ vlastnosti -- kvalitativní nebo kvantitativní vlastnosti závislé na objektech,
* vztah/typ vztahu -- propojení mezi dvěma (nebo více objekty), které je na nich závislé,
* událost/typ události -- nezávislé, v čase neměnné prvky (kompletně ukončené v minulosti).

Hodnotu atributu "Typ pojmu" pro pojem "Pozemková parcela" nastavíme na "Typ objektu".

**Pojem nemá zdroj**

Definice se skládá z textu a zdroje. Oba prvky jsou nutné ke 100 % validaci úplnosti pojmu. Jako zdroj pojmu "Pozemková parcela" vyplním "§ 2, d)".

**Pojem nemá rodiče**

Pojmy mezi sebou zpravidla mají hierarchické vztahy. Do atributu "Nadřazené pojmy" je možné vložit pojem ze stejného nebo importovaného slovníku (těmi se budeme zabývat pozdeji). Vybereme pojem "Parcela".

{% include figure image_path="/assets/images/tutorial-cs/opravy_chyb.png" alt="Opravy chyb editací pojmu" caption="Opravy chyb editací pojmu." %}

Změny potvrdíme stisknutím tlačítka "Uložit".

Ve spodní části detailu pojmu je záložka "Kontrola". Jejím otevřením zjistíme, že chyby u pojmu "Pozemková parcela" byly opraveny. Zároveň vidíme, že vedle názvu pojmu svítí zelené kolečko. V pravé části stránky -- v seznamu pojmů -- vidíme, že se vytvořila hierarchická relace mezi pojmy "Parcela" a "Pozemková parcela".

{% include figure image_path="/assets/images/tutorial-cs/hierarchie.png" alt="Nově vytvořená hierarchie mezi pojmy" caption="Nově vytvořená hierarchie mezi pojmy." %}

Editací můžete opravit i chyby dalších pojmů.

[comment]: <> Todo #### Závislost pojmů

### Anotace dokumentů

V této části tutoriálu budeme pracovat s dokumentem, který jsme nahráli při tvorbě slovníku. V detailu slovníku přepněte do záložky "Dokument" a tlačítkem "Obsah" u vašeho souboru ho zobrazte.

{% include figure image_path="/assets/images/tutorial-cs/zobrazení_souboru.png" alt="Zobrazení souboru přiřazeného slovníku" caption="Zobrazení souboru přiřazeného slovníku." %}

Slovník již obsahuje některé pojmy, které se ve slovníku nachází. Spustíme analýzu textu souboru pomocí našeho slovníku. Vpravo nahoře je tlačítko "Analyzovat". Po jeho stisknutí se objeví pop-up s roletovým menu, ze kterého vybereme slovník, podle kterého proběhne analýza textu. Výchozí je ten náš, necháme ho tam a stiskneme "Analyzovat".

{% include figure image_path="/assets/images/tutorial-cs/analyzovat.png" alt="Dialog pro výběr slovníku pro automatickou analýzu souboru" caption="Dialog pro výběr slovníku pro automatickou analýzu souboru." %}

Analýza může v závislosti na velikosti souboru a slovníku chvilku trvat. Výsledkem analýzy je návrh výskytů pojmů, které ve slovníku již existují a návrh nových pojmů a jejich výskytů.

{% include figure image_path="/assets/images/tutorial-cs/analýza.png" alt="Výsledek analýzy souboru" caption="Výsledek analýzy souboru." %}

#### Potvrzení výskytu pojmu

Pojmy označené zeleně s tečovaným ohraničením jsou navrhované výskyty existujících pojmů. Klikneme na návrh výskytu pojmu s textem "parcelou" v písmenu b) druhého paragrafu. Navrhovaným pojmem je "Parcela". Stisknutím fajfky výskyt potvrdíme. Tlačítko s ikonou tužky nabízí vybrat jiný pojem ze slovníku a malý odpadkový koš navrhovaný výskyt pojmu zahodí. Stisknutím křížku zavřeme pop-up. My výskyt potvrdíme a tím zmizí ohraničení pojmu.

{% include figure image_path="/assets/images/tutorial-cs/potvrzení_výskytu.png" alt="Potvrzení návrhovaného výskytu existujícího pojmu" caption="Potvrzení návrhovaného výskytu existujícího pojmu." %}

#### Vytvoření nového pojmu na základě návrhu

V písmenu a) druhého paragrafu je navržen výskyt doposud neexistujícího pojmu s textem "pozemkem". Rozhodneme se návrh přijmout. Kliknutím na označený text otevřeme podobný pop-up jako při potvrzování výskytu existujícího pojmu, ale s upozorněním, že *Fráze není přiřazena žádnému pojmu*. Kliknutím na ikonku tužky můžeme vybrat existující pojem, nebo vytvořit nový.

{% include figure image_path="/assets/images/tutorial-cs/vytvoření_nového_pojmu_návrh.png" alt="Vytvoření nového pojmu na základě návrhu výskytu neexistujícího pojmu" caption="Vytvoření nového pojmu na základě návrhu výskytu neexistujícího pojmu." %}

Po kliknutí na tlačítko "+ Nový" se otevře vyskakovací okno s dialogem velice podobným vytvoření pojmu ze slovníku s předvyplněným názvem podle vybraného textu. Text může být upraven. Nad políčkem Textu definice je zde nově tlačítko "Vybrat definici". To nám umožňuje vybrat definici přímo z textu. Stiskneme ho a označíme text ve zbytku písmene a druhého paragrafu. Po označení textu se vrátíme automaticky zpět do dialogu s již vyplněným textem definice. Vyplníme ještě zdroj "§ 2, a)", v pokročilých možnostech vybereme jako Typ pojmu "Typ objektu" a stiskneme "Vytvořit".

{% include figure image_path="/assets/images/tutorial-cs/vybrat_definici.png" alt="Dialog pro tvorbu pojmu z textu souboru" caption="Dialog pro tvorbu pojmu z textu souboru." %}

Po potvrzení vytvoření pojmu je pojem označen zeleně a jeho definice modře.

{% include figure image_path="/assets/images/tutorial-cs/výskyt+definice.png" alt="Označení výskytu pojmu a jeho definice" caption="Označení výskytu pojmu a jeho definice." %}

#### Vytvoření nového pojmu z textu

V písmenu e) druhého paragrafu se nachází pojem "geometrické určení", který není navržen jako výskyt pojmu. Pokud ho označíme myší, vyskočí pop-up dialog s dotazem, zda chceme označit výskyt pojmu, nebo jeho definici. Vybereme výskyt. Dále pokračujeme jako v případě vytvoření nového pojmu na základě návrhu.

{% include figure image_path="/assets/images/tutorial-cs/vybraný_text.png" alt="Výběr textu a volba mezi označením výskytu nebo definice" caption="Výběr textu a volba mezi označením výskytu nebo definice." %}

#### Označení definice

Druhou věcí, kterou je možné označit přímo v textu, je definice pojmu. Označíme definici pojmu "Parcela", který již text definice vyplněný má. Na řádku b) označte celý text od slovna pozemek na začátku až po čárku na konci. V pop-up okně zvolíme, že označujeme definici a z roletové nabídky vybereme pojem "Parcela". Vzhledem k tomu, že pojem již definici má, objeví se okno s porovnáním stávajícího i nového textu definice.

{% include figure image_path="/assets/images/tutorial-cs/změna_definice.png" alt="Porovnání stávajícího a nového textu definice" caption="Porovnání stávajícího a nového textu definice." %}

Text definice je možné upravovat, stejně jako její zdroj. Stisknutím tlačítka "Uložit" je změněn text definice pojmu a zároveň je v textu označena definice pojmu.
