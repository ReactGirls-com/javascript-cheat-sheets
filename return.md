Zde je cheat sheet pro klíčové slovo `return` v JavaScriptu:

1. **Účel `return`**

   - Klíčové slovo `return` se používá k ukončení funkce a navrácení hodnoty z funkce.

     ```javascript
     function soucet(a, b) {
       return a + b;
     }
     console.log(soucet(5, 3)); // Výstup: 8
     ```

2. **`return` bez hodnoty**

   - Pokud je `return` použito bez hodnoty, funkce vrátí `undefined`.

     ```javascript
     function ukonci() {
       console.log("Funkce ukončena");
       return;
     }
     console.log(ukonci()); // Výstup: undefined
     ```

3. **`return` ukončí funkci**

   - Jakmile je `return` vykonán, žádný další kód ve funkci se neprovede.

     ```javascript
     function test() {
       console.log("První řádek");
       return;
       console.log("Druhý řádek"); // Tento řádek nebude proveden
     }
     test(); // Výstup: První řádek
     ```

4. **`return` může vracet jakoukoli hodnotu**

   - `return` může vrátit jakýkoli typ dat v JavaScriptu, včetně objektů, polí, funkcí, atd.

     ```javascript
     function vytvorOsobu(jmeno, vek) {
       return {
         jmeno: jmeno,
         vek: vek,
       };
     }
     console.log(vytvorOsobu("Alice", 25)); // Výstup: { jmeno: 'Alice', vek: 25 }
     ```

5. **`return` může být použito k vrácení funkce z funkce**

   - `return` může být použito k vrácení funkce z funkce, což umožňuje koncepty jako funkce vyššího řádu. Ty jsou často použíté například v React useEffectu.

     ```javascript
     function vytvorPozdrav(jmeno) {
       return function () {
         console.log("Ahoj " + jmeno + "!");
       };
     }
     const pozdravAlice = vytvorPozdrav("Alice");
     pozdravAlice(); // Výstup: Ahoj Alice!
     ```

Klíčové slovo `return` je základním nástrojem pro řízení toku kódu a vrácení výsledků z funkcí v JavaScriptu.
