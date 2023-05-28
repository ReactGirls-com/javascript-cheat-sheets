Zde je cheat sheet pro definování tříd v JavaScriptu:

1. **Definice třídy**

   - Třídy v JavaScriptu se definují pomocí klíčového slova `class`.

     ```javascript
     class Osoba {
       constructor(jmeno, vek) {
         this.jmeno = jmeno;
         this.vek = vek;
       }
     }
     ```

2. **Konstruktor**

   - `constructor` je speciální metoda, kterou používáme k vytvoření a inicializaci objektu vytvořeného pomocí třídy.

     ```javascript
     class Osoba {
       constructor(jmeno, vek) {
         this.jmeno = jmeno;
         this.vek = vek;
       }
     }
     ```

3. **Metody třídy**

   - Třída může obsahovat metody.

     ```javascript
     class Osoba {
       constructor(jmeno, vek) {
         this.jmeno = jmeno;
         this.vek = vek;
       }

       pozdrav() {
         console.log(`Ahoj, jmenuji se ${this.jmeno} a je mi ${this.vek} let.`);
       }
     }
     ```

4. **Vytvoření instance třídy**

   - Instance třídy vytvoříme pomocí klíčového slova `new`.

     ```javascript
     const alice = new Osoba("Alice", 25);
     alice.pozdrav(); // Výstup: Ahoj, jmenuji se Alice a je mi 25 let.
     ```

5. **Klíčové slovo `new`**

   - Klíčové slovo `new` v JavaScriptu se používá k vytvoření instance objektu. Když použijete `new`, ve skutečnosti se volá metoda `constructor`, vytvoří se nový objekt, který dědí vlastnosti a metody dané třídy.

6. **Dědičnost**

   - Třídy v JavaScriptu podporují koncept dědičnosti pomocí klíčového slova `extends`.

     ```javascript
     class Zamestnanec extends Osoba {
       constructor(jmeno, vek, pozice) {
         super(jmeno, vek); // Zavolá constructor ve třídě Osoba
         this.pozice = pozice;
       }

       pozdrav() {
         super.pozdrav();
         console.log(`Pracuji jako ${this.pozice}.`);
       }
     }

     const bob = new Zamestnanec("Bob", 30, "programátor");
     bob.pozdrav();
     // Výstup: Ahoj, jmenuji se Bob a je mi 30 let. Pracuji jako programátor.
     ```

   - `super` se používá k volání funkcí na objektu rodiče.

Třídy v JavaScriptu jsou skvělým nástrojem pro organizaci kódu a implementaci konceptů objektově orientovaného programování.
