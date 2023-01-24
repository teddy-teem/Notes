# JavaScript Note:
 ## Mutability
> Javascript have 7 premitive data types, (string, number, bigint, bool, undefined, null, & symbol), these are immutable, We cannot change it's value, we only can reassign. 
Eexample bellow.
> ```
> let text = 'abcde'
> text[1] = 'z'
> console.log(text) //ans: abcde
> ```
> **N.B** Other types like object, function are mutable, theire value can be changed. 
> Example for Object (Array)
> ```
> const arr = [1,2,3]
> arr.length = 0
> console.log(arr) //arr of 0 length
> ```

## Accidental Global Variable
> ```
> (()=>{
>  let a = b = 0;
>  console.log(a, b); //a=0. b=0;
> })();
> console.log(a); // a isn't defined
> console.log(b); // 0
> ```
> The above program works as only ```a``` is ```let``` scoped variable, ```b``` is like ```window.b```, not with ```let``` scoped. This is called ***Accidental Global Variable***

## Coercion
> if ```2``` operands are connected with ```+``` operand, both operands will be changed to a string first with ```toString()``` method and then concatenated.
> The other operator such as ```-``` , ```*```, or ```/``` will change the operand to a number. If it cannot be coerced to a number, ```NaN``` will be returned.
> ```
> console.log(1 +  +"2" + "3"); //ans: 33
> console.log(1 +  -"1" + "3"); //ans: 03
> console.log(+"1" +  "1" + "3"); //ans: 113
> console.log( "A" - "B" + "2"); //ans: NaN2
> ```

## Sort
> ```
> const a = [1,5,2,10,3];
> console.log(a.sort()); //[1,10,2,3,5];
> ```
> if we ommitted the comparison function from sort(), the array elements are converted to strings, then sorted according to each character’s Unicode code point value.


