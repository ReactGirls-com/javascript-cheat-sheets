Zde je jednoduchý tahák, který ukazuje, kde a v jakém případě používáme různé typy závorek v JavaScriptu:

1. **Běžné závorky `()`**

   - **Deklarace a volání funkcí**: Používají se k uzavření parametrů při definování funkce a argumentů při volání funkce.

     ```javascript
     // Definice
     function pozdrav(jmeno) {
       console.log("Ahoj, " + jmeno);
     }

     // Volání
     pozdrav("Alice");
     ```

   - **Pořadí operací v aritmetice**: Označuje, které operace by měly být provedeny jako první.

     ```javascript
     let vysledek = (1 + 2) * 3; // vysledek je 9
     ```

   - **Seskupování výrazů**: Upřesňuje, jak by měly být výrazy vyhodnoceny.

     ```javascript
     let vysledek = ("Ahoj " + "světe!").toUpperCase(); // vysledek je "AHOJ SVĚTE!"
     ```

2. **Hranaté závorky `[]`**

   - **Definice a přístup k poli**: K definování pole a přístupu k jeho prvkům.

     ```javascript
     // Definice
     let ovoce = ["jablko", "banán", "třešně"];

     // Přístup
     console.log(ovoce[1]); // Výstup: banán
     ```

   - **Přístup k vlastnostem objektu**: K přístupu k vlastnostem objektu podle názvu, zejména když je název dynamický nebo není platným identifikátorem.

     ```javascript
     let osoba = {
       jmeno: "Bob",
       vek: 30,
     };

     let vlastnost = "vek";
     console.log(osoba[vlastnost]); // Výstup: 30
     ```

3. **Složené závorky `{}`**

   - **Definice objektu**: K definování objektu.

     ```javascript
     let osoba = {
       jmeno: "Bob",
       vek: 30,
     };
     ```

   - **Blok kódu**: Označuje blok kódu, pro funkce, smyčky, podmínky atd.

     ```javascript
     if (true) {
       console.log("Ahoj, světe!");
     }
     ```

   - **Šablony literálů**: K interpolaci proměnných nebo výrazů uvnitř šablony literálu (řetězec ohraničený zpětnými uvozovkami).

     ```javascript
     let jmeno = "Bob";
     console.log(`Ahoj, ${jmeno}!`); // Výstup: Ahoj, Bob!
     ``;
     ```

4. **Šipkové funkce `=>`**

   - **Šipková funkce s jednoduchým výrazem bez složených závorek `{}`**: Když má funkce pouze jeden výraz, není třeba používat složené závorky. V tomto případě je `return` implicitní.

     ```javascript
     // Funkce, která vrací druhou mocninu čísla
     let druhaMocnina = (cislo) => cislo * cislo;
     console.log(druhaMocnina(5)); // Výstup: 25
     ```

     Tato funkce vezme jedno číslo jako vstup (parametr `cislo`) a vrátí jeho druhou mocninu. Slovo `return` není v tomto příkladu uvedeno, ale je implicitní, protože funkce má pouze jeden výraz (`cislo * cislo`).

   - **Šipková funkce s více výrazy a složenými závorkami `{}`**: Pokud má funkce více výrazů, je třeba použít složené závorky a explicitně uvest slovo `return`.

     ```javascript
     // Funkce, která vypočítá obvod čtverce
     let obvodCtverce = (strana) => {
       let obvod = 4 * strana;
       return obvod;
     };
     console.log(obvodCtverce(5)); // Výstup: 20
     ```

     Tato funkce vezme jedno číslo jako vstup (parametr `strana`), vypočítá obvod čtverce (výraz `4 * strana`), uloží jej do lokální proměnné `obvod` a vrátí tento výsledek. Protože máme více než jeden výraz (definice proměnné a vrácení hodnoty), musíme použít složené závorky a explicitně uvest slovo `return`.
