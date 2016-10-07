### _Pre-Course Exercises_
###### **SKYLAB CODERS ACADEMY BOOTCAMP**_(Autumn 2016)_
[![SKYLAB ICON](https://camo.githubusercontent.com/7b3a7c3e9cdafad0258e05bbfd5b9d2ca38ba912/687474703a2f2f7777772e736b796c6162636f646572732e636f6d2f696d616765732f3430332f64656661756c742e706e67)](http://www.skylabcoders.com/es/)
### **_3.Conditionals_**
**_a)Let's start with simple exersice, declare your name, if your name is bigger than 8 letters, show a message_**

```javascript
    var myName= "Sergio";
    if(myName.length > 8) {
        console.log("You have a quite long name!")
    }
```

**_b) Add your lastname and compare separated_**

```javascript
    var myLastName = "Lucas";
    if(myLastName.length > 8) {
        console.log("You have a quite long name!")
    }
```

**_c) Now, compare between them and show who is bigger._**

```javascript
    if(myName.length > myLastName.length) {
        console.log("It looks like your name is longer!")
    } else {
        console.log("Interesting, your last name is longer than your name!")
    }
```

**_d) CALCULATOR. Multiply two numbers, so, compare the result with IF conditionals, if the result is > 10, show a message, if is < 10, show other message_**

```javascript
    var calculator = function (number1,number2){
        var resultado = number1 * number2;
        if ( resultado > 10){
            console.log("This number is bigger than 10");
        } else {
            console.log("This number is smaller than 10")
        }
    
    }
    calculator(2,2);
```

**_e) Then, what happen if we multiply 5*"word"? The result is NaN (Not a Number), then we can control this error with other conditional, right? Let's do this._**

```javascript
    var calculator = function (number1,number2){
        var resultado = number1 * number2;
        if ( resultado > 10){
            console.log("This number is bigger than 10");
        } else if (resultado < 10 ) {
            console.log("This number is smaller than 10")
        } else if ( isNaN(resultado) === true){
            console.log("Please, put only numbers")
        }

    }
    calculator(2,2);
```

**_f) CLOCK. Let's do other simply program that you pass one param. to a function, and the IF conditionals should print a message saying: Good morning/afternoon/night_**

```javascript
    var reloj = function(hour){
        hour = hour + ":00 "; // Para añadir el formato de hora.
        if ( 6 < hour < 12){
            console.log(" Good morning!");
        } else if ( 12 < hour < 19 ){
            console.log(" Good afternoon!");
        } else {
            console.log(" Good night!");
        }
    }
    reloj(6);
```

**_g) After that, now, compare with the local hour_**

```javascript
    var d = new Date(); // Te dice la fecha completa del <momento class="   "></momento>
    /*console.log(d);*/ 
    var n = d.getHours();// Solo coge la hora, sin minutos, de toda la información  que da new Date();
    /*console.log(n);*/
    var reloj = function(hour){
        if(hour < n){
            console.log("This hour is before now here in Spain.");
        } else {
            console.log("This hour is after now in Spain.");
        }
    }
    reloj(5);
    reloj(20);

```

**_h) IF the specify hour is equal to local hour? Control this exception!_**

```javascript
    var d = new Date();
    var n = d.getHours();
    var reloj = function(hour){
        if(hour < n){
            console.log("This hour is before now here in Spain.");
        } else if ( hour > n) {
            console.log("This hour is after now in Spain.");
        } else if ( hour === n){
            console.log("This is exactly the same hour here.");
        }
    
    }
    reloj(18);
```

**_i) BEATLES. Now we want to make a program that we specify the members of the Beatles, if are all the Beatles in the array, show "We're all!", if you specify 3 Beatles for example, say other thing._**

```javascript
    var beatles = ["a","b","c","d"];
    if (beatles.length === 4){
        console.log(" We are all!");
    }else {
        console.log(" Ups, is somebody missing?");
    }

```

**_j) Now, declare an empty array and do a function that PUSH the names of all Beatles, the conditional IF should return "We're all!"._**

```javascript
    var matriz = [];
    
    var beatlesName= function(name1,name2,name3,name4){ 
        matriz.push(name1,name2,name3,name4);// Poniendo el argumento de la función si que se introducen los valores correctamente pero si pones la funcion en si no lo reconoce.
        if (beatlesName.length === 4){
        console.log(" We are all!");
    }else {
        console.log(" Ups, is somebody missing?");
    }
    }
    beatlesName("a","b","c","d");
    console.log(matriz);

```

**_k) Make other program that push all Beatles, when the four Beatles are in array, show a message, if the length of a array are < 4, show a message that say to user: Continue writing the names! REMEMBER: Control the number of Beatles are in array after execute the function for sure you're pushing the names properly._**

```javascript
    var matrizBeatles = []; // Matriz vacía donde se van añadiendo a través de diferentes funciones los <diferent> </diferent>es <nombres class=""></nombres>
    var addBeatle1 = function(name1){   
        matrizBeatles.push(name1);// Permite añadir un valor a la matriz <vac>  </vac>ía
        total = matrizBeatles.length // la longitud de la array que permite controlar el push y el cumplimiento de las condiciones IF.
        if ( total === 4){
            console.log("You are right, we are all!");
        } else {
            console.log("Somebody else?...");
        }
    }
    addBeatle1("first");
    console.log(" Currently, we are " + total + " Beatles");
    
    var addBeatle2 = function(name2){ // La longitud de la array se  modifica al añadir valores y se controla la cantidad de nombres o datos stentes dentro   de la matriz.
        matrizBeatles.push(name2);
        total = matrizBeatles.length
        if ( total === 4){
            console.log("You are right, we are all!");
        } else {
            console.log("Somebody else?...");
        }
    }
    addBeatle2("second");
    console.log(" Currently, we are " + total + " Beatles");
    
    var addBeatle3 = function(name3){
        matrizBeatles.push(name3);
        total = matrizBeatles.length
        if ( total === 4){
            console.log("You are right, we are all!");
        } else {
            console.log("Somebody else?...");
        }
    }
    addBeatle3("third");
    console.log(" Currently, we are " + total + " Beatles");
    
    var addBeatle4 = function(name4){
        matrizBeatles.push(name4);
        total = matrizBeatles.length
        if ( total === 4){
            console.log("You are right, we are all!");
        } else {
            console.log("Somebody else?...");
        }
    }
    addBeatle4("fourth");
    console.log(" Currently, we are " + total + " Beatles");
    /*console.log(matrizBeatles);*/
```

**_I) RANDOM. Create a function that randomize a number and specify if the number are above or under the half of the maximum._**

```javascript
    var valorAleatorio = function(max,min){ 
        var valor= Math.floor(Math.random()*max + min); //Math.random()     proporciona numeros decimales entre 0 y 1 mientras que Math.floor()elimina los decimales y deja el numero entero.
        /*console.log(Math.random()*max);*/
        /*console.log(Math.random()*max + min);*/
        console.log(valor);
        if(valor > max / 2 ){
            console.log("This number is bigger than the half of " + max );
        }else if( valor < max / 2){
            console.log("This number is smaller than the half of " + max);
        }
    }
    
    valorAleatorio(20,10);
    
    /*console.log(Math.floor(Math.random()));*/
```


