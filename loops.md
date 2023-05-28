Zde je cheat sheet pro cykly v JavaScriptu:

1. **Cyklus `for`**

   - `for` cyklus se používá, když víte, kolikrát má cyklus běžet.

     ```javascript
     // Vypíše čísla od 0 do 4
     for (let i = 0; i < 5; i++) {
       console.log(i);
     }
     ```

2. **Cyklus `for...in`**

   - `for...in` cyklus prochází vlastnosti objektu.

     ```javascript
     let osoba = { jmeno: "Alice", vek: 25, zamestnani: "programatorka" };

     // Vyíše "jmeno: Alice"
     // Vyíše "vek: 25"
     // Vyíše "zamestnani: programatorka"
     for (let vlastnost in osoba) {
       console.log(`${vlastnost}: ${osoba[vlastnost]}`);
     }
     ```

3. **Cyklus `for...of`**

   - `for...of` cyklus prochází hodnoty iterovatelných objektů (například pole, mapy, sety).

     ```javascript
     let pole = ["jablko", "banán", "pomeranč"];

     // Vypíše všechny prvky pole
     for (let ovoce of pole) {
       console.log(ovoce);
     }
     ```

4. **Cyklus `while`**

   - `while` cyklus se opakuje, dokud je jeho podmínka pravdivá.

     ```javascript
     let i = 0;

     // Vypíše čísla od 0 do 4
     while (i < 5) {
       console.log(i);
       i++;
     }
     ```

5. **Cyklus `do...while`**

   - `do...while` cyklus je podobný `while` cyklu, ale vždy se provede alespoň jednou, neboť podmínka se vyhodnocuje až po provedení bloku kódu.

     ```javascript
     let i = 0;

     // Vypíše čísla od 0 do 4
     do {
       console.log(i);
       i++;
     } while (i < 5);
     ```

6. **Metoda `forEach`**

   - `forEach` je metoda pole, která provádí danou funkci pro každý prvek pole.

     ```javascript
     let pole = ["jablko", "banán", "pomeranč"];

     // Vypíše všechny prvky pole
     pole.forEach(function (ovoce) {
       console.log(ovoce);
     });
     ```
