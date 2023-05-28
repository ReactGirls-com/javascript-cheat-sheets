Zde je cheat sheet pro klíčové slovo `this` v JavaScriptu:

1.  **Základní použití `this`**

    - `this` se odkazuje na kontext, ve kterém byla funkce volána. V případě objektů `this` odkazuje na samotný objekt.

      ```javascript
      const objekt = {
        jmeno: "Alice",
        pozdrav: function () {
          console.log("Ahoj, jmenuji se " + this.jmeno);
        },
      };
      objekt.pozdrav(); // Výstup: Ahoj, jmenuji se Alice
      ```

2.  **`this` ve funkcích**

    - Pokud `this` použijeme ve funkci, která není metodou objektu, odkazuje na globální kontext (v prohlížeči na `window`).

      ```javascript
      function test() {
        console.log(this);
      }
      test(); // Výstup: Window {...}
      ```

3.  **`this` v konstruktoru**

    - V konstruktoru objektu `this` odkazuje na nově vytvořený objekt.

      ```javascript
      class Osoba {
        constructor(jmeno) {
          this.jmeno = jmeno;
      }

      const alice = new Osoba("Alice");
      console.log(alice.jmeno); // Výstup: Alice

      ```

4.  **`this` v událostech**

    - V případě událostí `this` odkazuje na element, který událost spustil.

      ```javascript
      button.addEventListener("click", function () {
        console.log(this); // `this` odkazuje na element button
      });
      ```

5.  **`this` v arrow funkcích**

    - Arrow funkce nevlastní svůj vlastní `this`. Místo toho dědí `this` z obklopujícího kontextu.

      ```javascript
      const objekt = {
        jmeno: "Alice",
        pozdrav: () => {
          console.log("Ahoj, jmenuji se " + this.jmeno);
        },
      };
      objekt.pozdrav(); // Výstup: Ahoj, jmenuji se undefined
      ```

Klíčové slovo `this` je základní součástí JavaScriptu a je nezbytné pro efektivní manipulaci s objekty a kontexty.
