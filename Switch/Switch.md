La **estructura switch es otra manera de evaluar condiciones, la diferencia con if es que las condiciones deben ser iguales a un caso o algo específico.

Cómo utilizar el condicional switch
Colocamos la palabra reservada switch y seguido de la variable o expresión a evaluar, pero sin ningún operador de comparación.

switch (expresion) {}
Después colocamos cada caso con la palabra reservada case y el valor que deberá ser igual a la expresión. Seguido colocamos el bloque de código a ejecutar y al final la palabra reservada break para que no vuelva a evaluar otra condición si ya se cumplió.

switch (expresion) {
    case 1: {
        // Bloque 1
        break
    }
    case 2: {
        // Bloque 2
        break
    }     
}
Finalmente, colocamos la condición por defecto con la palabra reservada default que se ejecutará si ninguno de los casos fue el correcto. Esto es semejante al bloque else.

switch (expresion) {
  case 1: {
    // Bloque 1
    break
  }
  case 2: {
   // Bloque 2
    break
  }
  default: {
    // Bloque por defecto
  }
}
Esto se leería de la siguiente manera: evalúa (switch) la variable expresion, en el caso de que sea igual a uno (case 1), entonces ejecuta el bloque 1 y termina (break), en el caso de que sea igual a dos (case 2), entonces ejecuta el bloque 2 y termina (break), si no se cumple ninguna, ejecuta un bloque por defecto (default).

Ejemplo utilizando switch
Por ejemplo, creemos un semáforo.

function semaforo(color) {
  switch (color) {
    case "verde": {
      console.log("¡Sigue!")
      break
    }
    case "amarillo": {
      console.log("¡Detente!")
      break
    }
    case "rojo": {
      console.log("¡No puedes avanzar!")
      break
    }
    default: {
      console.log("¡No reconozco ese color! :(")
    }
  }
}

semaforo("verde") //'¡Sigue!'
Cuándo utilizar switch
Deberías utilizar switch cuando tengas una gran cantidad de casos, que con el condicional if produciría más cantidad de código. El problema con switch es que no es muy utilizado y todo se resuelve con if. Sin embargo, conocer esta estructura te puede permitir escribir código más legible en ciertos casos.

Ejercicio de condicionales
Cambia tu juego de piedra, papel o tijera realizado con condicionales if a la estructura switch. ¿Qué diferencias observaste? ¡Comparte tu trabajo en la sección de aportes!

Contribución creada por Andrés Guano (Platzi Contributor).

Lecturas recomendadas

GitHub - degranda/jsBasico-: Ejemplos del curso de JS básico

https://github.com/degranda/jsBasico-