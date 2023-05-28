Zde je cheat sheet pro definování funkcí v JavaScriptu:

1. **Funkce deklarace**

   Funkce deklarace je nejtradičnější a nejběžnější způsob definování funkcí.

   ```javascript
   function pozdrav() {
     console.log("Ahoj světe!");
   }

   pozdrav(); // Výstup: Ahoj světe!
   ```

2. **Funkce jako výraz**

   Funkce výraz v JavaScriptu umožňujě přiřazení funkce do proměnné.

   ```javascript
   const pozdrav = function () {
     console.log("Ahoj světe!");
   };

   pozdrav(); // Výstup: Ahoj světe!
   ```

3. **IIFE (Immediately Invoked Function Expressions)**

   IIFE je funkční výraz, který se automaticky spustí, jakmile je definován.

   ```javascript
   (function () {
     console.log("Ahoj světe!");
   })(); // Výstup: Ahoj světe!
   ```

4. **Arrow funkce**

   Arrow funkce jsou zkrácenou syntaxí pro vytvoření funkčních výrazů. Neobsahují vlastní kontext `this`.

   ```javascript
   const pozdrav = () => {
     console.log("Ahoj světe!");
   };

   pozdrav(); // Výstup: Ahoj světe!
   ```

5. **Parametry a argumenty funkce**

   Funkce mohou přijímat vstupní data, která jsou označována jako parametry. Když funkci zavoláme a předáme do ní hodnoty, nazýváme je argumenty.

   ```javascript
   function pozdrav(jmeno) {
     console.log("Ahoj " + jmeno + "!");
   }

   pozdrav("Alice"); // Výstup: Ahoj Alice!
   ```

6. **Výchozí parametry funkce**

   JavaScript umožňuje nastavit výchozí hodnoty pro parametry funkce.

   ```javascript
   function pozdrav(jmeno = "světe") {
     console.log("Ahoj " + jmeno + "!");
   }

   pozdrav(); // Výstup: Ahoj světe!
   ```

7. **Funkce s návratovou hodnotou**

   Funkce mohou vracet hodnotu pomocí klíčového slova `return`.

   ```javascript
   function soucet(a, b) {
     return a + b;
   }

   console.log(soucet(2, 3)); // Výstup: 5
   ```

Funkce jsou základním stavebním kamenem v JavaScriptu a jsou nezbytné pro psaní modulárního a udržitelného kódu.
