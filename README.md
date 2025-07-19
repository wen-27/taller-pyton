ejercicio1: 
Escribe un programa que solicite al usuario una frase y muestre:

1. La cantidad total de caracteres en la frase.
2. La cantidad de espacios en la frase.

- definimos las tres variables necesarias las cuales son 
frase 
total_caracteres 
espacios 
- le pedimos la frase al usuario
frase = input("Escribe una frase: ")
- usamos la funcion len () para obtener la longitud de la frase 
total_caracteres = len(frase)
- hacemos uso de la funcion .count () para contar, la integramos de la siguiente forma en la cual ('' '') son los espacios en blanco
espacios = frase.count(" ")
- imprimimos el total de caracteres y el total de espacios usando la funcion f antes de el texto que nos permite unir variables en corchetes y expreciones 
print(f"La frase tiene {total_caracteres} caracteres en total.")
print(f"La frase tiene {espacios} espacios.")

ejercicio2:

Crea un programa que solicite al usuario su nombre completo y verifique:

1. Que solo contenga letras.
2. Que comience con mayúscula.

   - usar input y pedirle un nombre al usuario
     nombre = input("Escribe tu nombre completo: ")
   - usar nombre.replace(" ", ""): Este método toma la cadena nombre y crea una nueva versión de ella donde todos los caracteres de espacio (" ") han sido eliminados
     tambien  usamos .isalpha() Este método se aplica sobre la cadena ya sin espacios, Devuelve True si todos los caracteres de la cadena son letras del alfabeto (a-z, A-Z) y la cadena no está vacía.
      Si encuentra cualquier otro carácter (números, guiones, puntos, etc.), devuelve False
     
     if nombre.replace(" ", "").isalpha()
     
   - nombre.istitle(): Este método de cadena devuelve True si la cadena original (nombre) está en formato de "título"
      if nombre.istitle():
        print("El nombre es válido.")
   - else 
     Este bloque else corresponde a la primera condición if. Se ejecuta si nombre.replace(" ", "").isalpha() resultó ser False, lo que significa que la entrada del usuario contenía caracteres no permitidos como números, símbolos o signos de puntuación.
    
     else:
        print("El nombre debe comenzar con mayúscula.")
      else:
        print("El nombre solo debe contener letras.")

ejercicio3: 
      
Escribe un programa que pida al usuario una palabra y muestre la palabra invertida.

Usa el operador de slicing `[::-1]` para invertir la cadena.

  - preguntar al usuario con el input una palabra 
    palabra = input("Escribe una palabra: ")
  - definir la variable invertida para invertir la variable y usar el operado `[::-1]` para invertir la cadena.
    invertida = palabra[::-1]
  - imprimimos usando f' antes de el texto que nos permite unir variables en corchetes y expreciones
    print(f"La palabra invertida es: {invertida}")

ejercicio4:

Crea un programa que solicite al usuario una frase y reemplace todas las vocales por un carácter especial (*).
1. Usa `replace()` repetidamente para reemplazar las vocales.
2. Asegúrate de manejar tanto mayúsculas como minúsculas.

   - crear una variable llamada frase y usar input para solicitarle la frase al usuario:
     frase = input("Escribe una frase: ")
   - usamos el .remplace para remplazar los parametros que le indiquemos de la frase por un *
     frase_cifrada = frase.replace("a", "*").replace("e", "*").replace("i", "*").replace("o", "*").replace("u", "*")
      frase_cifrada = frase_cifrada.replace("A", "*").replace("E", "*").replace("I", "*").replace("O", "*").replace("U", "*")
   - imprimimos la frase con un f' antes para que nos permite unir variables en corchetes y expreciones
      print(f"La frase cifrada es: {frase_cifrada}")

ejercicio5: 

Escribe un programa que cuente cuántas vocales hay en una frase ingresada por el usuario.
1. Usa `count()` para contar las vocales individualmente.
2. Suma los resultados.

    - crear una variable llamada frase y usar input para solicitarle la frase al usuario:
      frase = input("Escribe una frase: ")
    - definir las variable, a , e, i , o ,u y usar el frase.cout para contar cuantas vocales en mayuscula o minuscula estan en la frase
      a = frase.count("a") + frase.count("A")
      e = frase.count("e") + frase.count("E")
      i = frase.count("i") + frase.count("I")
      o = frase.count("o") + frase.count("O")
      u = frase.count("u") + frase.count("U")
    - deinir una variable llamada total_vocales para sumar las vocales usadas
      total_vocales = a + e + i + o + u
    - imprimimos con print(f'') para nos permite unir variables en corchetes y expreciones
      print(f"La frase tiene {total_vocales} vocales.")

ejercicio6: 

Escribe un programa que tome un número de teléfono ingresado por el usuario (10 dígitos) y lo formatee como `(XXX) XXX-XXXX`.
1. Usa slicing para dividir la cadena en partes.
2. Usa `f-strings` o concatenación para formatear.

   - crear una variable llamada telefono y usar input para solicitarle la frase al usuario:
     telefono = input("Escribe un número de teléfono de 10 dígitos: ")
   - Esta línea es el núcleo de la validación y contiene dos condiciones unidas por un and, lo que significa que ambas deben ser verdaderas para que el bloque de código del if se ejecute.
  
   - len(telefono) == 10:
      La función len() devuelve la cantidad de caracteres en la cadena telefono.

   - == 10:
     Compara si esa longitud es exactamente igual a 10.
     
   - telefono.isdigit():
     .isdigit(): Es un método de las cadenas de texto que devuelve True si todos los caracteres de la cadena son dígitos numéricos (0-9) y la cadena no está vacía. Si encuentra cualquier otro carácter (como espacios, guiones, letras, etc.), devuelve False.
   - imprimimos con print(f'') para nos permite unir variables en corchetes y expreciones
      telefono[:3]: Extrae los caracteres desde el inicio (índice 0) hasta el índice 2 (el índice fin no se incluye). Esto corresponde a los 3 primeros dígitos (el código de área).
      
      telefono[3:6]: Extrae los caracteres desde el índice 3 hasta el 5. Esto corresponde a los siguientes 3 dígitos.
      
      telefono[6:]: Extrae los caracteres desde el índice 6 hasta el final de la cadena. Esto corresponde a los últimos 4 dígitos.

      telefono_formateado = f"({telefono[:3]}) {telefono[3:6]}-{telefono[6:]}"
        print(f"El número formateado es: {telefono_formateado}")

ejercicio7: 

Escribe un programa que determine si una palabra ingresada por el usuario es un palíndromo (se lee igual al derecho y al revés).
1. Usa slicing para invertir la palabra.
2. Compara la palabra original con la invertida.

   - crear una variable llamada palabra y usar input para solicitarle la frase al usuario el . lower es pR convertirme lo que ingresa el usuario en minusculas
      palabra = input("Escribe una palabra: ").lower()
   - definir la variable invertida para invertir la variable y usar el operado `[::-1]` para invertir la cadena.
      invertida = palabra[::-1]
   - =: El operador de igualdad compara el contenido de la variable palabra (la original, en minúsculas) con el contenido de la variable invertida.
    La comparación devuelve True si las cadenas son idénticas (como en el caso de "somos" y "somos") y False si no lo son (como en el caso de "python" y "nohtyp").
      if palabra == invertida:
   - print("La palabra es un palíndromo.")
      Este código se ejecuta solo si la condición del if es True. Informa al usuario que su palabra cumple con la definición de palíndromo.

   - else: print("La palabra no es un palíndromo.")
      Si la condición del if es False, el programa salta al bloque else e imprime el mensaje que indica que la palabra no es un palíndromo.

   

    


