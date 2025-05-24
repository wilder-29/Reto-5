Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_6 en slack.
 1. Dado la figura de la imagen, desarrolle:
![68747470733a2f2f692e706f7374696d672e63632f465276436d7078782f696d6167652e706e67](https://github.com/user-attachments/assets/80cfb272-4bef-4ae2-aeb9-2b16c563541f)
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
