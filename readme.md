# Creador de figuras (en trabajo)

Este programa crea las figuras que necesites dibujar.

## Requisitos

El programa necesita que le des numeros para elegir las distintas opciones.

```¿Como funciona?
```El programa es sencillo, solo ingresas los valores que quieres y te da una respuesta maravillosa.

## Código

```python
import os
def cerrarprograma():
  os.system("clear")
def triangulo(ancho):
  x = "x"*ancho
  for j in range(ancho):
    print(x[0:j+1])
  for z in reversed(range(ancho)):
    print(x[0:z])


def Xtriangulo(ancho):
  x = 'x'
  for j in range(ancho):
    print(x)
    x += "x"
  for z in reversed(range(ancho)):
    print(x[0:z])

tabla = []
alto = 82
cont1=0
largo = 42
for x in range(largo):
    for y in range(alto):
        if x == 0 or x == largo - 1:
            tabla.append(".")
        elif y == 0 or y == alto - 1:
            tabla.append(".")
        else:
            tabla.append(" ")
    matriz= ''.join(tabla)
    print(matriz)
    tabla=[]
print("MENU")
print()
print("1.Agregar una línea")
print()
print("2.Agregar una elipse o círculo")
print()
print("3.Agregar un rectángulo o cuadrado")
print()
print("4.Agregar un triángulo")
print()
print("5.Mostrar un Dibujo")
print()
print("6.Leer un dibujo")
print()
print("7.Grabar un dibujo")
print()
print("0.Cerrar programa")
print()
n = int(input("Selecciona una opción: "))
if n==0:
  cerrarprograma()
if n == 1:
  print("Por el momento solo funciona en diagonales con punto x y punto y iguales. Próximamente mejorará.")
  x1 = int(input("¿Cuál es el x del primer punto?: "))
  while not -1 < x1 < 83:
    print("Ha escrito un valor inválido para la línea. Escriba de nuevo")
    x1 = int(input("¿Cuál es el primer punto?: "))
  print("Listo")
  y1 = int(input("¿Cuál es el y del primer punto?: "))
  while not -1 < y1 < 43 :
    print("Ha escrito un valor inválido para la línea. Escriba de nuevo")
    y1 = int(input("¿Cuál es el y del primer punto?: "))
  print("Listo")
  x2 = int(input("¿Cuál es el x del segundo punto?: "))
  while not -1 < x2 < 83 :
    print("Ha escrito un valor inválido para la línea. Escriba de nuevo")
    x2 = int(input("¿Cuál es el x del segundo punto?: "))
  print("Listo")
  y2 = int(input("¿Cuál es el y del segundo punto?: "))
  while not -1 < y2 < 43 :
    print("Ha escrito un valor inválido para la línea. Escriba de nuevo")
    y2 = int(input("¿Cuál es el y del segundo punto?: "))
  print("Listo")
  for x in range(largo):
    for y in range(alto):
        if x == 0 or x == largo - 1:
            tabla.append(".")
        elif y == 0 or y == alto - 1:
            tabla.append(".")
        elif x==x1 and y==y1:
          tabla.append('x')
        elif x==x2 and y==y2:
          tabla.append('x')
        elif y2==y or y1==y:
          tabla.append(' ')
        elif x2>x>x1 and y1>y2:
          tabla.append(' ')
        elif x==y and x<x1 and x2<x:
          tabla.append('x')
        elif x==y and y<y1 and y2<y:
          tabla.append('x')
        elif x==y and x<x2 and x1<x:
          tabla.append('x')
        elif x==y and y<y2 and y1<y:
          tabla.append('x')
        elif x!=y:
          tabla.append(' ')
        else:
            tabla.append(" ")
    matriz= ''.join(tabla)
    print(matriz)
    tabla=[]
if n==2:
  xc1=int(input("Ha seleccionado elipse/círculo, escriba la coordenada y del centro: "))
  while not -1<xc1<43:
    print("No está dentro de los valores de la matriz. Escriba de nuevo. ")
    xc1=int(input("Ha seleccionado elipse/círculo, escriba la coordenada y del centro: "))
  yc1=int(input("Escriba la coordenada x del centro: "))
  while not -1<yc1<43:
    print("No está dentro de los valores de la matriz. Escriba de nuevo. ")
    yc1=int(input("Escriba la coordenada x del centro: "))
  print()
  print("Para utilizar un círculo, escriba 1")
  print()
  print("Para utilizar un elipse, escriba 2")
  print()
  ec=int(input("¿Utilizará un elipse o un círculo? "))
  if ec==1:
    r=int(input("Ingrese el radio del círculo: "))
    print("Listo")
    rm=r//2
    dobler=2*r
  else:
    r1=int(input("Ingrese el radio vertical de la elipse"))
    print("Listo")
    print()
    r2=int(input("Ingrese el radio horizontal de la elipse"))
    print("Listo")
  for x in range(largo):
    for y in range(alto):
        if x == 0 or x == largo - 1:
            tabla.append(".")
        elif y == 0 or y == alto - 1:
            tabla.append(".")
        elif x == xc1 and y == yc1:
          tabla.append('x')
        elif x==xc1+r+1 and yc1==y:
          tabla.append('x')
        elif y==yc1+r+1 and xc1==x:
          tabla.append('x')
        elif x==xc1-r-1 and yc1==y:
          tabla.append('x')
        elif y==yc1-r-1 and xc1==x:
          tabla.append('x')
        elif y==yc1-r and xc1<x<yc1+r+1:
          tabla.append('x')
        elif y==yc1+r and xc1<x<yc1+r+1:
          tabla.append('x')
        elif y==yc1-r and xc1-r-1<x<xc1:
          tabla.append('x')
        elif y==yc1+r and xc1-r-1<x<xc1:
          tabla.append('x')
        elif x==xc1+r and yc1-r<y<yc1+r:
          tabla.append('x')
        elif x==xc1-r and yc1-r<y<yc1+r:
          tabla.append('x')
        else:
          tabla.append(' ')
    matriz= ''.join(tabla)
    print(matriz)
    tabla=[]
if n==3:
  er=int(input("Para rectángulo 1, para cuadrado 2: "))
  while not 0<er<3:
    print("Ha escrito un valor inválido, escriba de nuevo. ")
    er=int(input("Para rectángulo, el número uno. Para cuadrado, el número 2:  "))

  if er==1:
    print("Ha seleccionado un rectángulo/cuadrado.")
    print()
    rc1x=int(input("Escriba el centro (x) : "))
    while not -1<rc1x<83:
      print("El valor no está dentro de lo aceptado, escriba de nuevo. ")
      rc1x=int(input("Escriba el centro (x) : "))

    rc1y=int(input("Escriba el centro (y) : "))
    while not -1<rc1y<43:
      print("El valor no está dentro de lo aceptado, escriba de nuevo. ")
      rc1y=int(input("Escriba el centro (y) : "))
    rlh=int(input("Cuánto es el lado horizontal?: "))
    rlh2=rlh//2
    rlv=int(input("Cuánto es el lado vertical?: "))
    rlv2=rlv//2
    
  for x in range(largo):
    for y in range(alto):
        if x == 0 or x == largo - 1:
            tabla.append(".")
        elif y == 0 or y == alto - 1:
            tabla.append(".")
        elif x == rc1x and y == rc1y:
          tabla.append('x')
        elif y== rc1y+rlh2 and x==rc1x:
          tabla.append('x')
        elif y==rc1y-rlh2 and x==rc1x:
          tabla.append('x')
        elif x==rc1x+rlv2 and y==rc1y:
          tabla.append('x')
        elif x==rc1x-rlv2 and y==rc1y:
          tabla.append('x')
        elif x==rc1x-rlv2 and rc1y-rlh2-1<y<rc1y+rlh2+1:
          tabla.append('x')
        elif x==rc1x+rlv2 and rc1y-rlh2-1<y<rc1y+rlh2+1:
          tabla.append('x')
        elif y==rc1y+rlh2 and rc1x-rlv2-1<x<rc1x+rlv2+1:
          tabla.append('x')
        elif y==rc1y-rlh2 and rc1x-rlv2-1<x<rc1x+rlv2+1:
          tabla.append('x')
        else:
          tabla.append(' ')
    matriz= ''.join(tabla)
    print(matriz)
    tabla=[]
if n==4:
  print("Ha seleccionado triángulo.")
  ancho1=int(input("Escriba el lado mayor del triángulo: "))
  print(xtriangulo(ancho1))
```

## Contribuciones:
Gracias a Diego por ayudar con el ppt y profesor, espero que esto sea de su agrado.
