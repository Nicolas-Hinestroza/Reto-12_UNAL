# Reto-12_UNAL
Desarrolle la mayoría de ejercicios en clase, por cado punto resuelto en clase tendrá media décima en el examen 2 (creanme, las van a necesitar). Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_11 en slack.


- **1.Consulte que hacen los siguientes métodos de strings en python**

- **Endswith**

El método Endswith() devuelve True si una cadena termina con el sufijo especificado. Si no, devuelve False.

    texto = "Python es facil de aprender."
    resultado = texto.endswith('de aprender') 
    # returns False
    print(resultado)
    resultado = texto.endswith('de aprender.')
    # returns True
    print(resultado)
    resultado = texto.endswith('Python es facil de aprender.')
    # returns True
    print(resultado)

- **Startswith**

El método startswith() devuelve True si la cadena comienza con el valor especificado; de lo contrario, False.

    texto = "Python es facil de aprender."
    resultado = texto.startswith('Python') 
    # returns True
    print(resultado)
    resultado = texto.startswith('de aprender.')
    # returns False
    print(resultado)
    resultado = texto.startswith('Python es facil de aprender.')
    # returns True
    print(resultado)

- **Isalpha**

El método isalpha() devuelve True si todos los caracteres son letras del alfabeto (a-z).

    texto = "Company"
    resultado = texto.isalpha()
    # returns True
    print(resultado)
    texto_2 = "Company10"
    resultado_2 = texto_2.isalpha()
    #returns False
    print(resultado_2)

- **Isalnum**

El método isalnum() devuelve True si todos los caracteres son alfanuméricos, es decir, letras del alfabeto (a-z) y números (0-9).

    texto = "Python"
    resultado = texto.isalnum()
    # returns True
    print(resultado)
    texto_2 = "Python10"
    resultado_2 = texto_2.isalnum()
    #returns True
    print(resultado_2)

- **Isdigit**

El método isdigit() devuelve True si todos los caracteres son dígitos, de lo contrario, False.

    texto = "Python Es Facil De Aprender"
    resultado = texto.isdigit()
    # returns False
    print(resultado)
    texto_2 = "12345"
    resultado_2 = texto_2.isdigit()
    #returns True
    print(resultado_2)

- **Isspace**

El método isspace() devuelve True si todos los caracteres de una cadena son espacios en blanco; de lo contrario, False.

    texto = "  "
    resultado = texto.isspace()
    # returns True
    print(resultado)
    texto_2 = "Python10"
    resultado_2 = texto_2.isspace()
    #returns False
    print(resultado_2)

- **Istitle**

El método istitle() devuelve True si todas las palabras de un texto comienzan con una letra mayúscula Y el resto de la palabra son minúsculas; de lo contrario, False. El método istitle() devuelve True si todas las palabras de un texto comienzan con una letra mayúscula, Y el resto de la palabra son letras minúsculas, de lo contrario Falso.

    texto = "Python Es Facil De Aprender"
    resultado = texto.istitle()
    # returns True
    print(resultado)
    texto_2 = "Python Es facil de aprender"
    resultado_2 = texto_2.istitle()
    #returns False
    print(resultado_2)

- **Islower**

El método islower() devuelve True si todos los caracteres están en minúsculas, de lo contrario, False.

    texto = "Python Es Facil De Aprender"
    resultado = texto.islower()
    # returns False
    print(resultado)
    texto_2 = "python es facil de aprender"
    resultado_2 = texto_2.islower()
    #returns True
    print(resultado_2)

- **Isupper**

El método isupper() devuelve True si todos los caracteres están en mayúsculas, de lo contrario, False.

    texto = "Python Es Facil De Aprender"
    resultado = texto.isupper()
    # returns False
    print(resultado)
    texto_2 = "PYTHON ES FACIL DE APRENDER"
    resultado_2 = texto_2.isupper()
    #returns True
    print(resultado_2)

- **2.Procesar el archivo y extraer:**

- **Cantidad de vocales**

![image](https://github.com/Nicolas-Hinestroza/Reto-12_UNAL/assets/124611099/bd1f34a5-c9e7-41ee-be9f-62b17faed29e)

    with open("Texto.txt", 'r') as archivo: # Definimos el archivo a abrir
        contenido = archivo.read() # se lee el texto 

    def contar_vocales(texto): # Definimos la funcion con la variable texto
        vocales = 'a','e','i','o','u','A','E','I','O','U'  # Escribimos las vocales en minúsculas y mayusculas
        contador = 0 # se inicia el recuento
        for letras in texto:  # se buscan los digitos 
            if letras in vocales: # Si letras esta en vocales entonces haga
                contador += 1 # Sumarle 1 al contador
        return contador # Nos devuelve el resultado

    cantidad = contar_vocales(contenido)  # definimos la variable cantidad como el resultado de la funcion
    print("La cantidad de vocales en el texto es: {}".format(cantidad)) # se imprime el resultado

- **Cantidad de consonantes**

![image](https://github.com/Nicolas-Hinestroza/Reto-12_UNAL/assets/124611099/ee23cea4-4910-4a45-90ac-0f7d63a37f5d)

    with open("Texto.txt", 'r') as archivo: # Definimos el archivo a abrir
        contenido = archivo.read() # se lee el texto 

    def contar_Consonantes(texto):# Definimos la funcion con la variable texto
        vocales = 'a','e','i','o','u','A','E','I','O','U'  # Escribimos las vocales en minúsculas y mayusculas
        contador = 0 # se inicia el recuento
        for letras in texto:  # se buscan los digitos 
            if letras.isalpha() and letras not in vocales: # Si letyras es un caracter alfabetico y no pertenece a vocales entonces haga
                contador += 1 # Sumarle 1 al contador
        return contador # Nos devuelve el resultado

    cantidad = contar_Consonantes(contenido)  # definimos la variable cantidad como el resultado de la funcion
    print("La cantidad de vocales en el texto es: {}".format(cantidad)) # se imprime el resultado

- **Listado de las 50 palabras que más se repiten**

![image](https://github.com/Nicolas-Hinestroza/Reto-12_UNAL/assets/124611099/7615b7df-d9d8-4d9f-8171-cb9e6242079a)

    from collections import Counter # utilizamos collections y Counter para realizar un seguimiento de los elementos y su recuento.
    import re # Usamos este modulo para encontrar operaciones de coincidencia

    def obtener_palabras_mas_comunes(Texto): # Definimos la funcion con la variable texto
        with open(Texto, 'r') as Archivo: # Definimos el archivo a abrir
            contenido = Archivo.read() # se lee el texto  
            palabras = re.findall(r'\w+', contenido.lower()) # Definimos palabras utilizando el modulo el cual nos Devuelve todas las coincidencias de las palabras en minuscula 
            frecuencia = Counter(palabras) # Para la frecuencia usamos el modulo para tener un contador de las palabras
            palabras_comunes = frecuencia.most_common(50) # Definimos la variable con una frecuencia de las 50 palabras mas comunes 
        return palabras_comunes # Nos devuelve las palabras comunes
    
    palabras_mas_comunes = obtener_palabras_mas_comunes("Texto.txt") # LLamamos la funcion con el texto deseado
    Contador = 0 # se inicia el recuento
    print("Listado de las 50 palabras más repetidas:") # Imprimimos el enunciado
    for palabra, frecuencia in palabras_mas_comunes: # Para las palabras y su frecuencia en las palabras comunes imprima cada palabra y cada frecuencia
        Contador += 1 # Sumarle 1 al contador
        print("#{}. La palabra {}: aparecio {} veces" .format(Contador, palabra, frecuencia)) # se imprime el resultado

- **Listado de destinatarios con cantidad de mensajes recibidos**

![image](https://github.com/Nicolas-Hinestroza/Reto-12_UNAL/assets/124611099/572b67d0-eab0-4654-8789-31c799df17f6)

    def destinatarios_mensanjes(archivo): # Definimos la funcion con la variable texto
       cuenta_destinatarios = {}  # Diccionario para almacenar los destinatarios y la cantidad de mensajes recibidos
   
       with open(archivo, 'r') as archivo_texto: # Definimos el archivo a abrir
           for line in archivo_texto:  # con el for vamos a recorrer cada linea del texto
               linea = line.strip()  # Definimos linea como la line con los espacios al principio y fin eliminados
               if linea.startswith("To:"): # la linea inicia con To: entonces haga
                   destinatario = linea[4:].strip()  # Definimos destinatario como la linea con el To: eliminado
                   cuenta_destinatarios[destinatario] = cuenta_destinatarios.get(destinatario, 0) + 1  # Usamos el diccionario para almacenar los destinatarios y con get nos devuelve los destinatarios
   
       print("Listado de destinatarios con cantidad de mensajes recibidos:") # Imprimimos el enunciado 
       for destinatario, cuenta in cuenta_destinatarios.items(): # Para los destinatarios y su cuenta en la cuenta_destinatarios con el objetivo 
           print(f"{destinatario}: {cuenta} mensajes") # se imprime el resultado

    destinatarios_mensanjes("Texto.txt") # LLamamos la funcion con el texto deseado

- **Cantidad de mensajes enviados por cada día**

