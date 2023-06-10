Los condicionales son estructuras de control que te permiten evaluar diferentes expresiones y realizar determinadas acciones en JavasScript.

Cómo utilizar el condicional ifen JavaScript
Un condicional evalúa si una expresión o condición es verdadera. Por ejemplo, si mi edad es mayor o igual que 18, puedo conducir.

if (edad >= 18){
    console.log("Puedes conducir")
}
La palabra reservada else evalúa cuando la expresión del if es falsa, pero no es obligatorio colocarlo. En el ejemplo anterior, la condición contraria del if es la edad menor que 18, entonces no puedes conducir.

if (edad >= 18){
    console.log("Puedes conducir")
} else {
    console.log("No puedes conducir")
}
En otras palabras, si (if) una acción (expresión) es verdadera (true) hago una acción (bloques de código). En el caso contrario (else) efectúo otra acción.

Cómo anidar condicionales al programar
Has aprendido a usar un condicional, pero ¿y si tenemos varias condiciones? Entonces empleamos las palabras reservadas else if junto a la condición a ejecutar, puedes utilizar varias condiciones que necesites. Sin embargo, JavaScript evalúa la primera condición, luego a la segunda, y así sucesivamente. Esto es importante para ordenar las condiciones correctamente y no sobreescribirlas.

if (condicion1){
   // Bloque 1
} else if (condicion2){
    // Bloque 2
} else if (condicion3){
   // Bloque 3
} else {
    // Bloque else
}
Por ejemplo, un cliente solicita un descuento según el número de artículos que ha comprado, la tienda ofrece 3 descuentos: 10% si ha comprado hasta 5 artículos, 15% hasta 10 artículos, y todo por encima de 10 artículos recibe un 20% de descuento. Dependiendo de la condición, el resultado será diferente.

function calcularDescuento(articulos, precio) {
  var precioFinal

  if (articulos <= 5) {
    //Hasta 5 artículos
    precioFinal = precio * (1 - 0.1)
  } else if (articulos > 5 && articulos <= 10) {
    //De 6 a 10 artículos
    precioFinal = precio * (1 - 0.15)
  } else {
    //De 10 artículos en adelante
    precioFinal = precio * (1 - 0.2)
  }

  return precioFinal
}

calcularDescuento(4, 10) // 9
calcularDescuento(8, 20) // 17
calcularDescuento(15, 50) // 40
Operador ternario
El operador ternario consiste en evaluar si una expresión es verdadera o falsa. Parecido a un condicional, pero en una línea de código. Esto sirve para evaluar una condición de manera rápida. La estructura que sigue es la siguiente y se lee como: "La condición es verdadera (?), si es así ejecuta el “Bloque verdadero”, caso contrario (:), ejecuta el “Bloque falso”.

condicion ? Bloque verdadero : Bloque falso
Por ejemplo, guardemos en una variable un mensaje si un número es par o impar.

function esPar(numero){
    return numero % 2 === 0 ? "Es par" : "No es par"
}

esPar(2) // "Es par"
esPar(3) // "No es par"
Ejercicio de condicionales
Crea el juego de piedra, papel o tijera. Te dejo una pequeña ayuda para este reto:

Genera las variables correspondientes
Produce los condicionales que comparen tu resultado con el de la máquina u otra persona.
Encapsula los condicionales en una función que reciba las variables, compararlas y retornar un valor.
¡Comparte tu trabajo en la sección de aportes!

Contribución creada por Andrés Guano (Platzi Contributor).

Lecturas recomendadas

Operador condicional (ternario) - JavaScript | MDN

https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Operadores/Conditional_Operator


GitHub - degranda/jsBasico-: Ejemplos del curso de JS básico

https://github.com/degranda/jsBasico-