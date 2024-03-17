# PVA4 - Programování a vývoj aplikací
## Lekce 23: OOP - Dědičnost - souhrn

## Obsah

Pokračujeme ve zpracování předchozím cvičením. Příklady 1 a 2 jsme zpracovávali minulou hodinu. Zdrojové kódy si zkopírujte a dnes na ně navážeme příklady 3 a 4.

### 1 Streaming
Uvažuj, že vyvíjíš software pro službu, která nabízí streamování videa. Služba nabízí dva typy pořadů - filmy a seriály. Firma chce evidovat, které filmy a seriály nabízí a jejich žánry. Dále chce u filmů evidovat délku a u seriálů počet episod a délku jedné episody.

Vytvoř program, který bude obsahovat tři třídy - `Pořad`, `Film` a `Seriál`.
- Třída `Pořad` bude sloužit jako základ pro další třídy. Bude mít atributy určující název a žánr. Oba atributy jsou povinné. K atributům přistupuj výhradně za použití get/set metod.
- Třída `Film` bude potomkem třídy `Pořad`. Film má kromě názvu a žánru atribut délka a rok vydání.
- Třída `Seriál` bude potomkem třídy `Pořad`. Má kromě názvu a žánru atributy počet epizod a délka epizody.

Všem třídám přidej funkci getInfo(), která vypíše informace o pořadu, resp. o filmu a seriálu. Funkce u třídy `Pořad` vypíše název a žánr. Následně tuto funkci využij ve funkcích u tříd Film a Serial a přidej k ní informaci o délce, resp. počtu episod.

Po naprogramování si vytvoř alespoň jeden objekt reprezentující film a seriál o ověr, že vše funguje.


### 2 Shlédnutí
Služba nyní eviduje uživatele, kteří službu využívají. Vytvoř třídu Uživatel, která bude mít atributy uživatelské jméno a délka sledování (v minutách), který udává celkovou délku pořadů, které uživatel zhlédl. Uživatelské jméno získej jako parametr a délka sledování je na začátku 0.

Třídám Serial a Film přidej funkce pro zjištění celkové délky, která vrátí celkovou délku filmu/seriálu (u seriálu je to počet episod násobený délkou jedné epizody).

Třídě Uzivatel přidej funkci pro nápočet délky zhlédnutí, která bude mít jeden parametr. Funkce zvýší atribut udávající celkovou délku sledování o hodnotu parametru.

Vytvoř objekt, který reprezentuje nějakého uživatele. Následně zkus uvažovat situaci, že uživatel zhlédne film a seriál, které jsi vytvořil(a) jako objekty. Uživateli připočti délky pořadů k délce sledování. 

Zjisti celkovou délku shlédnutí videí uživatele. Výsledek zobraz uživateli v podobě `x dní, x hodin x minut`. Není-li délka shlédnutí alespoň jeden den, část x dní nezobrazuj. Obdobně pro hodiny.

### 3 Historie uživatele
Rozšiř vlastnosti a metody našeho programu o sledování, jaké pořady uživatel sledoval. Vytvoř si ukázkové objekty a ověř, že vše funguje.

### 4 Statistika platformy
Z pohledu platformy nyní mám evidenci pořadů i evidenci uživatelů. Víme jaké pořady jednotliví uživatelé shlédli. Pro provoz platformy chcete znát základní statistické údaje. Zjistěte hodnoty následujících KPI:
- nejoblíbenější pořad
- uživatele s nejvíce shlédnutými pořady
- průměrný počet shlédnutých pořadů za uživatele
- průměrný počet shlédnutýh minut na uživatele
- nejoblíbenější pořad aktuálního roku
