### _Pre-Course Exercises_
###### **SKYLAB CODERS ACADEMY BOOTCAMP**_(Autumn 2016)_
[![SKYLAB ICON](https://camo.githubusercontent.com/7b3a7c3e9cdafad0258e05bbfd5b9d2ca38ba912/687474703a2f2f7777772e736b796c6162636f646572732e636f6d2f696d616765732f3430332f64656661756c742e706e67)](http://www.skylabcoders.com/es/)
### **_3.Challenges_**
**_a) FINAL!We turn back to numbers... So, we want do a programm that execute the Fibonacci serie_**

```javascript
    var fib= []; // Se inicializa una array vacía para introducir los valores de la secuencia.

    for (var i = 2 ; i <= 10; i++) {
        fib[0]= 0;// Se introducen los dos primeros valores a la array para que funcione el loop correctamente.
        fib[1]= 1;

        fib[i]= fib[i-2] + fib[i-1];// Fibonacci x^n = x^n-1 + x^n-2 ;
                                // El resultado es el valor de la suma del valor anterior a este y el dos veces anterior.
    }

    console.log(fib);
```

**_b) You can add the position of all sums?_**

```javascript
    for (var i= 0 ; i < fib.length ; i++){ // Se recorre la array con todos los valores y se añade su posicion con lastIndexOf().
        console.log(fib[i] + "," + " pos " + fib.lastIndexOf(fib[i]));
    }
```

**_c) You can now specify the number of loops that the function must do?_**

```javascript
    var fibo= function(num){ // se establece que la length del array es el parametro de la función. Después, se hace un console del numero de veces que se ha ejecutado el loop.
        for (var i= 0 ; i <= num ; i++){
        console.log(fib[i] + "-" + " pos " + fib.lastIndexOf(fib[i]) + "th");
        }
    };
    fibo(10);
```

**_d) Simple Scripting program. Create a program that transform a 4 number values code to diferents positions, making a new code. Something like: 3712 👇 7123 👇 1237 👇 2371 The first, go to the last position, second, third and four goes up._**

```javascript
    var matriz1 = [3, 7, 1, 2];

    var cambioDePosicion = function(matriz) {
        var primerElemento = matriz[0]; // variable para definir el primer elemento de la array.

        for (var i = 0; i < matriz.length - 1; i++) { // Se pone -1 en la length para modificar manualmente el ultimo valor que cumple otra condición.
            matriz[i] = matriz[i + 1]; // Se recorre la array y se mueven todos los numeros excepto el ultimo.
        }

        matriz[i] = primerElemento; // Se establece que para el proximo valor de i > matriz.length-1 el valor sea el primer elemento definido antes del loop.

        return matriz;
    }

    for (var i = 0; i < matriz1.length; i++) {
        console.log(matriz1);
        matriz1 = cambioDePosicion(matriz1); // de esta forma se enseñan todas las modificaciones que sufriría cumpliendose las condiciones una y otra vez.
    }
```

**_e) Super-Challenge!! Create a program that use the Roman form for encrypt messages, how is that? Simple. If you have SKYLAB, the encrypted form is SLKAYB... If you divided the word in two groups of 3 letters, you get: SKY |-|-| LAB Then, join the S with L, K with A and Y with B, and you get SLKAYB.

So, make a program that, receive the message SKYLAB and returns the SLKAYB._**

```javascript
    var textC = "SKYLAB";
    var SUBSTRING_LENGHT = 3;
    /*console.log(gru1);
    console.log(gru2);*/
    var encrypt = function(cadena){
        var textEnc = ''; // Es necesario crear una string vacía donde plasmar la palabra encriptada
        var gru1 = cadena.substring(0, SUBSTRING_LENGHT); // con el substring, se hacen dos grupos con la palabra de tres letras cada uno.
        var gru2 = cadena.substring(SUBSTRING_LENGHT, SUBSTRING_LENGHT*2);

        for (var i = 0 ; i < SUBSTRING_LENGHT ; i++) {
        /*console.log(textC[i]);*/
            textEnc += gru1[i] + gru2[i] // se coge la primera letra de los dos grupos formados y se hace una especie de push en string.
        }

        return textEnc;
    }
    console.log(encrypt(textC));
    console.log(textEnc);
```

**_f) Now, you can do the DECRYPTER? Pass the ENCRYPTED message (SLKAYB) and returns SKYLAB. Hint:: for decrypt, only catch the pair words like: SLKAYB , then, you get SKY, the next step is catch the odd words, SLKAYB group the two groups and you get the original word._**

```javascript
    var decrypt = function(cadena1){
         var par = ""; // Se establecen las dos cadenas vacías para añadir las letras pares y las impares por separado.
        var impar = "";

        for (i = 0 ; i < cadena1.length; i++) { // Se recorre la string y se compara su indice .
        //console.log(cadena1[i]);
            if(i % 2 === 0) { // Si es par, se añadirá la letra en la variable en cuestión.
            par += cadena1[i];
            } else {
            impar += cadena1[i];
            }
        }

        return par + impar; // Aquí se obtiene la palabra de nuevo desencriptada.
    }

//console.log(decrypt(encrypt(textC)));

```

**_g) Group the Encrypt and decrypt functions in one unique function, pass the word SKYLAB and returns SKYLAB (with all the transformation...)_**

```javascript
    var encryptDecrypt = function(cadena) {
        return decrypt(encrypt(cadena)); //la funcion ejecuta las dos funciones definidas anteriormente.
    }

    console.log(encryptDecrypt("SKYLAB"));

```

**_h) You got it? Then try now with SKYLABCODERS. Reform the program for can accept more large words._**

```javascript
    var textToEnc= "SKYLABCODERS";

    var encrypt12= function (palabra){
        var encryword="";
        var gr1= palabra.substring(0,3);
        var gr2= palabra.substring(3,6);
        var gr3= palabra.substring(6,9);
        var gr4= palabra.substring(9,12);

        for (var i = 0 ; i < gr1.length ; i++){
            encryword += gr1[i] + gr2[i] + gr3[i] + gr4[i];
        }

        return encryword
    }
    console.log(encrypt12(textToEnc));

    var decrypt12= function(palabra){
        var par1= "";
        var impar1= "";
        var par2= "";
        var impar2="";

    for ( var i=0 ; i < palabra.length ; i++){
        if ( i % 2 === 0){
            par1 += palabra[i];
        } else if ( i % 2 !== 0){
            impar1 += palabra[i];
        }
    }

    var almAns= par1 + impar1;

    for ( var i=0 ; i < almAns.length ; i++){
        if ( i % 2 === 0){
            par2 += almAns[i];
        } else if ( i % 2 !== 0){
            impar2 += almAns[i];
        }
    }

    return par2 + impar2;
    }
    console.log(decrypt12(encrypt12(textToEnc)));

    var encryptDecrypt12=function(palabra){
        return decrypt12(encrypt12(palabra));
    }

    console.log(encryptDecrypt12(textToEnc));
```

