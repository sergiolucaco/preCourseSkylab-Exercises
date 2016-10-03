### _Pre-Course Exercises_
###### **SKYLAB CODERS ACADEMY BOOTCAMP**_(Autumn 2016)_
[![SKYLAB ICON](https://camo.githubusercontent.com/7b3a7c3e9cdafad0258e05bbfd5b9d2ca38ba912/687474703a2f2f7777772e736b796c6162636f646572732e636f6d2f696d616765732f3430332f64656661756c742e706e67)](http://www.skylabcoders.com/es/)
### **_1.Strings_**
**_a)Define a string var with your name b) Now, show your name in console terminal_**

```javascript
    var name="Sergio";
    console.log(name);
```

**_c) Fine, now, define a var with your age and show your age and name also using the console_**

```javascript
    var age= 24;
    console.log(name + age);
```

**_d) Pass this vars as parameters in a function that shows them on the console_**

```javascript
    var showMyData= function (name,age){
    console.log(name + " " + age);
    };
    showMyData("Sergio", 24);
```

**_e) Now, show your info with a pretty presentation message_**

```javascript
    var showMyData= function(name,age){
        console.log("My name is "+ name + " and I am " + age + " years old");
    };
    showMyData("Sergio",24);

```

**_f) Add a new parameter to the function for your current city, Can you RETURN the updated presentation message?_**

```javascript
    var showMyData= function(name,age,city){
        console.log("My name is "+ name + " and I am " + age + " years old and I live in " + city);
    var myData= showMyData("Sergio",24,"Barcelona");
    console.log(myData);

```

**_g) Modify your function to receive data in an array. Should return the same_**

```javascript
    var showMyData= function ([name,age,city]){
        console.log("My name is "+ name + " and I am " + age + " years old and I live in " + city);
    }
    var myData= showMyData(["Sergio", 24 ,"Barcelona"]);
    console.log(myData);
```

**_h) Modify your function to return the string "ERROR!" if second parameter is not a number_**

```javascript
    var showMyData= function([name,age,city]){
        if (typeof age == "number"){ // Condicion para comprobar que sea un numero la variable en cuestion.
        console.log("My name is "+ name + " and I am " + age + " years old and I live in " + city);
        } else {
        console.log("ERROR!");
        }
        };
    var myData= showMyData(["Sergio","sergio","Barcelona"]);
    console.log(myData);
```

**_i) Modify your function to receive values in a string separated by '|'. Should return the same (also the error logic)_**

```javascript
    var showMyData= function(cadena){
        var resultado = cadena.split('|');// Se hace un split de la string para convertirla en array y luego escoger los elementos uno a uno. Se ha de  escoger el separador.
        var cadenaANumero = parseInt(resultado[1]);// Convierte una string en numero.
        if (typeof cadenaANumero == "number"){ // Condicion para comprobar que sea  un numero la variable en cuestion. 
        console.log("My name is "+ resultado[0] + " and I am " + cadenaANumero + "  years old and I live in " + resultado[2]);
        } else {
        console.log("ERROR!");
        }
    };
    var myData= showMyData("Sergio|24|Barcelona");
    console.log(myData);
```

**_j) Add a new function to your program that insert a new value in the array, asure the changes are completed in console._**

```javascript
    var array = ["value1","value2"];  
    var addValue = function(value){
        array.push(value);
    }
    addValue("value3"); 
    console.log(array);// se le da valor a la función y luego se printea la array que modifica dicha función por si sola.
```

**_k) Now, after insert some new values, modify the function for return the array values separated by '&'._**

```javascript
    var devolverCadena = function(matriz){
        return matriz[0] + "&" + matriz[1] + "&" + matriz[2];// Para añadir separadores en los elementos de un array conociendo la longitud.
    } 
    console.log(devolverCadena(array));
```

