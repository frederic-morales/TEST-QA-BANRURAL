## Error No1

Al momento de ingresar un dato al input y enviar el formulario con el botón no se muestra ningun mensaje ya sea "Correcto" o "Incorrecto", ya que la propiedad "addEventListener" del input de tipo "submit" esta mal escrita, por lo que no se enviaba el dato ingresado por el usuario, propiedad mal escrita "addeventListener" la solucion sería "addEventListener"
.

## Error No2

Al momento de enviar el formulario con el botón no se muestra el mensaje de que si el número es mayor o menor, el error esta en que al momento de asignar el elemento "p" a la constante lowOrHi con "document.querySelector" no esta reconociendo el elemento p con la clase "lowOrHi" ya que no se le esta agregando el "." antes del nombre de la clase, la solución sería "document.querySelector(".lowOrHi")"

## Error No3

Al momento de ingresar un numero que no sea un numero entero no se muestra ninguna alerta al usuario y además se incrementa el número de intentos del usuario, condicion al inicio de la funcion para verificar si se esta ingresando un número entero:

- if (!Number.isInteger(parseFloat(userGuess))) {
- guesses.textContent = "Debe ingresar un número entero"
- return
- }

## Error No4

Al momento de ingresar el ultimo intento, se muestra que el usuario ganó y que adivino el número y esto es incorrecto ya que este mensaje se esta mostrando cuando el usuario utilice su ultimo intento y solo se debería de mostrar cuando el usuario adivine el numero, el error esta en los condicionales if, condiciones cambiadas:

- if (guessCount === ATTEMPS) {
- lastResult.textContent = '!!!Pérdistes!!!';
- lastResult.style.backgroundColor = 'black';
- lowOrHi.textContent = '';
- setGameOver();
- } else if (userGuess == randomNumber) {
- lastResult.textContent = 'Felicitaciones! adivinaste el número!';
- lastResult.style.backgroundColor = 'red';
- setGameOver();
- }.

## Error No5

El numero a adivinar puede ser un número decimal, esto es incorrecto ya que el usuario solo puedo ingresar numeros enteros por lo que el usuario estaría ingresando un numero entero y se estaría comparando con un numero decimal. Solucion: agregar "Math.floor" a la variable "randomNumber"

## Error No6

Al momento de terminar el juego, ya sea que el usuario gané o pierda el se ejecuta la funcion "setGameOver" no se reiniciba el juego porque la propiedad "addEventListener" del boton "resetButton" estaba mal escrita.

## Error No7

Numero de intentos 5, los requerimientos indican que el usuario debe de tener 10 intentos, la solución sería cambiar la variable ATTEMSP = 10
