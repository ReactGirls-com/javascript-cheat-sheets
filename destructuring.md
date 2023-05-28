**Destrukturalizace** je skvělý nástroj pro čistší a srozumitelnější kód, pokud je správně používán.

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
