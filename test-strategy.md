## Error No1

Al momento de ingresar un dato al input y enviar el formulario con el botón no se muestra ningun mensaje ya sea "Correcto" o "Incorrecto", ya que la propiedad "addEventListener" del input de tipo "submit" esta mal escrita, por lo que no se enviaba el dato ingresado por el usuario.

## Error No2

Al momento de enviar el formulario con el botón no se muestra el mensaje de que si el número es mayor o menor, el error esta en que al momento de asignar el elemento "p" a la constante lowOrHi con "document.querySelector" no esta reconociendo el elemento p con la clase "lowOrHi" ya que no se le esta agregando el "." antes del nombre de la clase, la forma correcta sería "document.querySelector(".lowOrHi")"

## Error No3

Al momento de ingresar un numero que no sea un numero entero no se muestra ninguna alerta al usuario y además se incrementa el número de intentos del usuario, condicion al inicio de la funcion para verificar si se esta ingresando un número entero:
if (!Number.isInteger(parseFloat(userGuess))) {
guesses.textContent = "Debe ingresar un número entero"
return
}

## Error No4

Al momento de ingresar el ultimo intento, se muestra que el usuario ganó y que adivino el número y esto es incorrecto ya que este mensaje se esta mostrando cuando el usuario utilice su ultimo intento y solo se debería de mostrar cuando el usuario adivine el numero.
