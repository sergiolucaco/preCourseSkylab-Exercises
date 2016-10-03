### _Pre-Course Exercises_
###### **SKYLAB CODERS ACADEMY BOOTCAMP**_(Autumn 2016)_
![SKYLAB ICON](https://camo.githubusercontent.com/7b3a7c3e9cdafad0258e05bbfd5b9d2ca38ba912/687474703a2f2f7777772e736b796c6162636f646572732e636f6d2f696d616765732f3430332f64656661756c742e706e67)
### **_2.Loops_**
**_a) We want to do a counter, from 0 to 5._**

```javascript
    for (var i=0 ; i < 6; i++){
        console.log(i)
    }
```
**_b) You can add a message when the count is over?_**

```javascript
    for (var i=0 ; i < 6; i++){
        console.log(i)
    }
    console.log("Count has finished");// Una vez finalice la loop, aparecerá el mensaje
```
**_c) Now we want to increase the count to 10. d) You can do the same, but with an array?_**

```javascript
    for (var i=0 ; i < 11; i++){
        console.log(i)
    }
    console.log("Count has finished");
    var matriz = [0,1,2,3,4,5,6,7,8,9,10];
    for (var i=0; i< matriz.length ; i++ ){
        console.log(matriz[i]);
    }
```
**_e) So, how about create a friend list? Change the array values for your friends names and show in console._**

```javascript
    var matriz = ["pepe","juan","manolo","nameN"];
    for (var i=0; i< matriz.length ; i++ ){
        console.log(matriz[i]);
    }
```

**_f) Now we want add a number, show for console the array position of your friends behind their names._**

```javascript
    var matriz = ["pepe","juan","manolo","nameN"];
    for (var i=0; i< matriz.length ; i++ ){// recorre toda la matriz.
        console.log(matriz[i] + " - num. " + matriz.lastIndexOf(matriz[i]));// muestra el recorrido de toda la matriz y se le añade la posición de la matriz con .lastIndexOf().
    }
```

**_g) You can add a last friend into a array? Show the updated array for console._**

```javascript
    var matriz = ["pepe","juan","manolo","nameN"];
    var addFriend = "francisco";
    matriz.push(addFriend);//se añade a la matriz un nuevo elemento en la ultima posición de esta.
    for (var i=0; i< matriz.length ; i++ ){
        console.log(matriz[i] + " - num. " + matriz.lastIndexOf(matriz[i]));
    }
```

**_h) create a loop for show in console the results from 0 to 50 in 5 to 5._**

```javascript
    var sum = 0 // Es necesario generar una variable adicional para empezar por 0 y que se vaya actualizando a cada loop que va incrementando su valor en 1.
    for (var i=0 ; i<=10;i++){
        sum = sum + i; // En el primer loop, sum = 0 , i = 0 . En el siguiente loop, sum=0 mientras que i=1, por tanto 1. En la siguiente, sum=1 y i=2. Asi que en el siguiente loop, sum = 3 e i = 3, es decir 6, etc.
        console.log(sum);// Asi se consigue sumar al valor actual el valor anterior,(0+0),(0+1),(1+2),(2+3).. En este ejercicio se consigue realizar un Count de las i que a su vez se sumen a un valor inicial, otorgado por la variable sum.
    }
```

**_i) Now, modify your program for shows the results to 0 to 100, in 10 to 10._**
```javascript
    //Se deben pasar los valores sumados a una array para poder poner su posición.
    var sum = 0; // Es necesario generar una variable adicional para empezar por 0 y que se vaya actualizando a cada loop que va incrementando su valor en 1.
    var matriz=[];// Se crea una array vacía para introducir todos los valores obtenidos del loop generado.
    for (var i=0 ; i<=10;i++){
        sum = sum + i; 
        console.log(sum);
        matriz.push(sum);// La keyword necesaria para ir añadiendo en último lugar uno a uno todos los valores obtenidos del loop.
    }
    for (var i=0 ; i < matriz.length ; i++){ // variable loop para recorrer toda la array (matriz[i]) y así poder poner su posición con last.IndexOf().
    console.log(matriz[i] + "- num " + matriz.lastIndexOf(matriz[i]));
    }
```




