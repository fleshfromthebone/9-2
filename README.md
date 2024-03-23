# 9-2 `NULL`s and `VOID`s and `UNDEFINED`s galore

## Please remember to define variables.
- `Undefined`: a parameter or value that has not been assigned a value. Does not entirely mean "no value", just unspecified.

```
let age;
```
See, nothing assigned. Just left like that. Usually, you do NOT want to do this, not sure what kind of situation I would ever have to assign a value like this.

- `Null` is when there is no value assigned at all. Not 0 or unassigned, nothing. on purpose.

```
let age = null
```
- `Not defined` is much different from undefined. It means that the value does not exist at all. Say I try to get a parameter that doesn't exist
```
console.log(finalAge)
```
This will cause an error because that parameter does not even exist, so no value has been assigned to it.

Not to be mixed with `NaN`, or "not a number".

## Composite data types

- In some instances, data can be bundled up and put into one line, instead of just having to write `const` or `let` over and over and over, we can write an Array with various elements, similar to a list
- Elements are ordered starting from 0, and can be called with with that assigned position,
```
const craftingMaterials = ["Wood", "Iron", 64, "Diamonds", 32]
console.log(craftingMaterials[0]); // Wood
console.log(craftingMaterials[2]); // 64
```
### Speaking of `const`

For a while, a good portion of us (me included to be honest) want to think `const` means constant. In some instances, it can be if thou is working with primitive data.

However, this is not the case at times. Especially if working with arrays where the data can be reassigned, even with a `const` in the line.
```
craftingMaterials[0] = "sand"
console.log(craftingMaterials[0] //sand
```
Now our array is mutated and our code is filled with sand 😠

A good solution to avoid instances like this is to write them as Object Literals.

### Avoid function scoping problems and utilizing Object Literals

- Objects, or object literals, are similar to arrays, except with alot more structure and direct references to the values assigned within.
```
const houseParts = {
floorFlavor: "Mahogany"
floorPlanks: 32;
hoaApproved: false;
};

console.log (houseParts[floorFlavor]); // Getting the value via bracket notation
console.log (houseParts.floorPlanks); // Dot notatin. Do it however you please I am not your God.
```

Object literals, arrays, or any composite data type can be useful when using functions that may not be able to utilize primitive data types as easily.<br/>
Otherwise you get what happened to me during Thursday's assignments 🙃<br/>
If a variable is declared inside of the function, it won't be accessible anywhere else. It's possible to access variables from outside the function scope though that is not recommended. <br/

_Important note_: Do not type a variable both inside and outside the function with the same name. This is known as variable shadowing and only confuses both you and the code.
