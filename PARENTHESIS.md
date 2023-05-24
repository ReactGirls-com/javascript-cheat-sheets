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

4. **Destrukturalizace** je skvělý nástroj pro čistší a srozumitelnější kód, pokud je správně používán.

   - **Destrukturalizace pole**: Používá se k rozdělení hodnot z pole do samostatných proměnných.

     ```javascript
     // Pole
     let ovoce = ["jablko", "banán", "třešně"];
     let [prvniOvoce, druheOvoce] = ovoce;
     console.log(prvniOvoce); // Výstup: jablko
     console.log(druheOvoce); // Výstup: banán
     ```

   - **Destrukturalizace objektu**: Používá se k rozdělení vlastností z objektu do samostatných proměnných.

     ```javascript
     // Objekt
     let osoba = {
       jmeno: "Bob",
       vek: 30,
     };

     let { jmeno, vek } = osoba;
     console.log(jmeno); // Výstup: Bob
     console.log(vek); // Výstup: 30
     ```

   - **Destrukturalizace ve funkčních parametrech**: Používá se k přímému přístupu k vlastnostem objektu nebo hodnotám pole předaným jako parametry funkce.

     ```javascript
     // Objekt
     function vypisOsobu({ jmeno, vek }) {
       console.log(`Jmeno je ${jmeno}, vek je ${vek}.`);
     }
     vypisOsobu(osoba); // Výstup: Jmeno je Bob, vek je 30.

     // Pole
     function vypisOvoce([prvni, druhe]) {
       console.log(`První ovoce je ${prvni}, druhé ovoce je ${druhe}.`);
     }
     vypisOvoce(ovoce); // Výstup: První ovoce je jablko, druhé ovoce je banán.
     ```
