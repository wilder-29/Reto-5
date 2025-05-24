Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_6 en slack.
 1. Dado la figura de la imagen, desarrolle:
![68747470733a2f2f692e706f7374696d672e63632f465276436d7078782f696d6167652e706e67](https://github.com/user-attachments/assets/80cfb272-4bef-4ae2-aeb9-2b16c563541f)

    Una función matemática para calcular el volumen y el área superficial.
    Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.
    Revise como utilizar el valor de pi usando import math y math.pi

Desarrollo.


    import math

    def calcular_volumen(r1, r2, h):
    
    #Debemos calcular el volumen de un cilindro con una semiesfera en la parte superior
    #r1: radio del cilindro
    #r2: radio de la semiesfera
    #h: altura del cilindro
    volumen_cilindro = math.pi * r1**2 * h
    volumen_semiesfera = (2/3) * math.pi * r2**3
    return volumen_cilindro + volumen_semiesfera

    def calcular_area_superficial(r1, r2, h):
    
    #Ahora debemos calcular el área superficial del cilindro con una semiesfera en la parte superior
    #r1: radio del cilindro
    #r2: radio de la semiesfera
    #h: altura del cilindro

    area_lateral_cilindro = 2 * math.pi * r1 * h
    area_base_cilindro = math.pi * r1**2
    area_semiesfera = 2 * math.pi * r2**2
    return area_lateral_cilindro + area_base_cilindro + area_semiesfera

    # Solicitar valores
    r1 = float(input("Ingrese el radio del cilindro : "))
    r2 = float(input("Ingrese el radio de la semiesfera : "))
    h = float(input("Ingrese la altura del cilindro : "))

    # Calcular y mostrar resultados
    volumen = calcular_volumen(r1, r2, h)
    area = calcular_area_superficial(r1, r2, h)
    # Al imprimir el resultado final, en algunos casos nos puede dar muchos decimales por lo que podemos 
    # indicarle la camtidad de decimales que queremos indicando con un (.3f),(.2f)...
    print(f"Volumen total: {volumen:.3f}")
    print(f"Área superficial total: {area:.3f}")

  
  2. Dado la figura de la imagen, desarrolle:
      ![68747470733a2f2f692e706f7374696d672e63632f3174344d727a734c2f696d6167652e706e67](https://github.com/user-attachments/assets/ed049e48-17cb-4e87-a7f4-8477fc97583a)
      
   Una función matemática para calcular el área y el perimetro.
   Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b.
   Revise como utilizar el valor de pi usando import math y math.pi
Desarrollo.

    import math

    def calcular_area(r, a, b):
    
    # Debemos calcular el área de un sector circular con lados a y b
    # Asumo que es un sector circular donde a y b son ángulos o longitudes de arco
    # Asumo que es un sector circular con ángulo central a (en radianes) 
    return 0.5 * r**2 * a

    def calcular_perimetro(r, a, b):
    
    # Calcular el perímetro de la figura (sector circular + lados)
    # Longitud del arco (radio * ángulo) + los dos radios
    return r * a + 2 * r

    r = float(input("Ingrese el radio : "))
    a = float(input("Ingrese el primer parámetro : "))
    b = float(input("Ingrese el segundo parámetro : "))

    area = calcular_area(r, a, b)
    perimetro = calcular_perimetro(r, a, b)

    print(f"Área: {area:.2f}")
    print(f"Perímetro: {perimetro:.2f}")

3. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.
Desarrollo.

       def calcular_carne_aves(G, M, P):

       # Aqui debemos calcular la cantidad total de carne de aves
       # G: número de gallinas (6 kg cada una)
       # M: número de gallos (7 kg cada uno)
       # P: número de pollitos (1 kg cada uno)

       # Se multiplica la candidad de aves por el peso de cada una
    
       return G * 6 + M * 7 + P * 1
 
       G = int(input("Ingrese el número de gallinas: "))
       M = int(input("Ingrese el número de gallos: "))
       P = int(input("Ingrese el número de pollitos: "))
  
       cantidad_total_carne = calcular_carne_aves(G, M, P)
       print(f"Cantidad total de carne de aves: {cantidad_total_carne} kg")
   

   4. Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.
   
          def calcular_prestamo(c, i, n):
    
          # Calcular el valor futuro de un préstamo con interés compuesto
          # c: capital inicial
          # i: tasa de interés mensual (en decimal, ej. 5% = 0.05)
          # n: número de meses
          return c * (1 + i)**n

          c = float(input("Ingrese el capital inicial del préstamo: "))
          i = float(input("Ingrese la tasa de interés mensual (ejemplo. 0.05 para 5%): "))
          n = int(input("Ingrese el número de meses: "))

          valor_futuro = calcular_prestamo(c, i, n)
          print(f"Valor futuro del préstamo: {valor_futuro:.2f}")

   5. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:

   El promedio
   El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
   La potencia del mayor número elevado al menor número
   La raíz cúbica del menor número

   Respuesta

       import math

       def promedio(numeros):
           return sum(numeros) / len(numeros)

       def promedio_multiplicativo(numeros):
           return (numeros[0] * numeros[1] * numeros[2] * numeros[3] * numeros[4]) ** (1/5)

       def potencia_mayor_menor(numeros):
           mayor = max(numeros)
           menor = min(numeros)
        return mayor ** menor

       raiz_cubica_menor(numeros):
           menor = min(numeros)
           return menor ** (1/3)

       n1 = float(input("Ingrese el número 1: "))
       n2 = float(input("Ingrese el número 2: "))
       n3 = float(input("Ingrese el número 3: "))
       n4 = float(input("Ingrese el número 4: "))
       n5 = float(input("Ingrese el número 5: "))
 
       numeros = [n1, n2, n3, n4, n5]

 
       print(f"Promedio: {promedio(numeros):.2f}")
       print(f"Promedio multiplicativo: {promedio_multiplicativo(numeros):.2f}")
       print(f"Potencia del mayor elevado al menor: {potencia_mayor_menor(numeros):.2f}")
       print(f"Raíz cúbica del menor número: {raiz_cubica_menor(numeros):.2f}")

6. Consultar qué es y cómo funciona pip en python.
pip es el sistema de gestión de paquetes por defecto para Python. Su nombre significa “Pip Installs Packages” y permite instalar, actualizar y desinstalar paquetes o módulos que no están incluidos en la biblioteca estándar de Python.
¿Cómo funciona?

    Fuente de paquetes: pip descarga e instala paquetes desde el Python Package Index (PyPI), un repositorio en línea que contiene miles de bibliotecas de Python.

    Uso básico en consola:
   
       pip install nombre-del-paquete

pip también permite:
Ver qué paquetes están instalados: pip list
Actualizar paquetes: pip install --upgrade nombre
Desinstalar: pip uninstall nombre
Guardar/leer un listado de dependencias: pip freeze > requirements.txt

Requisitos: pip viene instalado por defecto en Python 3.4+ (si usas python.org o anaconda).


7. Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.

Listado de módulos populares que se pueden instalar con pip y cómo instalarlos
Módulo	¿Para qué sirve?	Comando de instalación
NumPy	Computación científica y manipulación de arreglos y matrices	pip install numpy
Pandas	Análisis y manipulación de datos en estructuras tipo tabla	pip install pandas
Matplotlib	Visualización de datos con gráficos (barras, líneas, pastel, etc.)	pip install matplotlib
scikit-learn	Aprendizaje automático y minería de datos	pip install scikit-learn
requests	Realizar solicitudes HTTP (GET, POST, etc.) a APIs o sitios web	pip install requests
Flask	Crear aplicaciones web ligeras en Python	pip install flask
Django	Framework completo para desarrollo web robusto	pip install django
BeautifulSoup	Extraer datos de páginas web (web scraping)	pip install beautifulsoup4
PyGame	Crear videojuegos en Python	pip install pygame
OpenCV	Visión por computadora y procesamiento de imágenes	pip install opencv-python
Seaborn	Visualización estadística basada en Matplotlib	pip install seaborn
TensorFlow	Machine learning y deep learning desarrollado por Google	pip install tensorflow
PyTorch	Deep learning desarrollado por Facebook	pip install torch
SQLAlchemy	ORM para manejar bases de datos con Python	pip install SQLAlchemy
FastAPI	Framework moderno y rápido para crear APIs REST	pip install fastapi

   


