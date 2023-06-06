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

- **Cantidad de consonantes**

- **Listado de las 50 palabras que más se repiten**

- **Listado de destinatarios con cantidad de mensajes recibidos**

- **Cantidad de mensajes enviados por cada día**

