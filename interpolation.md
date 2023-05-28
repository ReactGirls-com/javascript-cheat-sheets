Zde je cheat sheet pro práci s interpolací řetězců v JavaScriptu:

1. **Sčítání řetězců (Concatenation) pomocí `+`**

   - Tato metoda se často používala před zavedením šablonových literálů v ES6. Sčítáme řetězce a proměnné dohromady.

     ```javascript
     let jmeno = "Alice";
     console.log("Ahoj, " + jmeno + "!"); // Výstup: Ahoj, Alice!
     ```

2. **Interpolace pomocí šablonových literálů (Template Literals)**

   - Šablonové literály, označované zpětnými uvozovkami (`` ` ``), umožňují vkládání proměnných nebo výrazů přímo do řetězců pomocí syntaxe `${...}`.

     ```javascript
     let jmeno = "Alice";
     console.log(`Ahoj, ${jmeno}!`); // Výstup: Ahoj, Alice!
     ```

3. **Interpolace s výrazy**

   - Šablonové literály umožňují nejen vkládání proměnných, ale také jakýchkoli platných JavaScriptových výrazů.

     ```javascript
     let x = 5;
     let y = 10;
     console.log(`Součet čísel je ${x + y}.`); // Výstup: Součet čísel je 15.
     ```

4. **Multiliniové řetězce**

   - Šablonové literály umožňují snadno vytvářet multiliniové řetězce bez nutnosti používat speciálních znaků, jako je `\n` pro nový řádek.

     ```javascript
     let jmeno = "Alice";
     let pozdrav = `Ahoj,
     ${jmeno}!`;
     console.log(pozdrav);
     /* Výstup:
     Ahoj,
     Alice!
     */
     ```
