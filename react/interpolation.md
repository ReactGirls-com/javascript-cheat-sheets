Zde je cheat sheet pro práci s interpolací v JSX a Reactu:

1. **Interpolace proměnných**

   - Pro vložení proměnných do JSX se používají složené závorky `{}`.

     ```jsx
     const jmeno = "Alice";
     const pozdrav = <h1>Ahoj, {jmeno}!</h1>; // Vypíše: Ahoj, Alice!
     ```

2. **Interpolace výrazů**

   - Do JSX lze vkládat jakýkoli platný JavaScriptový výraz pomocí složených závorek `{}`.

     ```jsx
     const x = 10;
     const y = 20;
     const soucet = <h1>Součet čísel je {x + y}.</h1>; // Vypíše: Součet čísel je 30.
     ```

     ```jsx
     const jmeno = "Alice";
     const pozdrav = <h1>{`Ahoj, ${jmeno}!`}</h1>; // Vypíše: Ahoj, Alice!
     ```

3. **Podmíněná interpolace**

   - Lze použít ternární operátor pro podmíněnou interpolaci.

     ```jsx
     const jeRegistrovan = true;
     const pozdrav = (
       <h1>
         {jeRegistrovan ? "Vítej zpět, Alice!" : "Prosím zaregistrujte se."}
       </h1>
     );
     // Vypíše: Vítej zpět, Alice!
     ```

4. **Interpolace komponent**

   - Komponenty lze také interpolovat v JSX.

     ```jsx
     const Pozdrav = () => <h1>Ahoj, Alice!</h1>;
     const App = () => <div>{<Pozdrav />}</div>; // Vypíše: Ahoj, Alice!
     ```

5. **Interpolace polí**

   - Pole lze také interpolovat v JSX.

     ```jsx
     const pole = ["Alice", "Bob", "Charlie"];
     const seznam = (
       <ul>
         {pole.map((jmeno) => (
           <li>{jmeno}</li>
         ))}
       </ul>
     );
     ```

   - Poznámka: Při mapování polí do JSX by měl být každému prvku přiřazen unikátní `key` prop.

Pamatujte, že při interpolaci v JSX musí být vše uzavřeno v jedné kořenové JSX značce nebo fragmentu (`<> </>`).
