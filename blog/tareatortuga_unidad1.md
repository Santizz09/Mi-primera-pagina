```python


# Esta variable guarda la posición horizontal actual de la tortuga
posicion = 0

# Esta lista guarda todo el recorrido para imprimirlo al final
recorrido = []


def avanzar(pasos):
    # Esta función dibuja la línea horizontal del avance.
    # Uso guiones para el camino y '>' para representar la cabeza de la tortuga.
    global posicion
    linea = "-" * pasos + ">"
    recorrido.append(linea)
    posicion += pasos  # Actualizo la posición


def bajar(pasos):
    # Esta función dibuja la bajada vertical.
    # Uso tantos espacios como la posición actual para que quede alineado.
    global posicion
    for i in range(pasos):
        linea = " " * posicion + "|"
        recorrido.append(linea)


# INICIO DEL PROGRAMA
print("Simulador de tortuga escalonada")
print("------------------------------")

# Pregunto al usuario cuántos escalones quiere
escalones = int(input("¿Cuántos escalones quieres dibujar? : "))

for i in range(escalones):
    print(f"\n--- Escalón {i+1} ---")
    pasos_avance = int(input("¿Cuántos pasos avanza la tortuga? : "))
    pasos_bajada = int(input("¿Cuántos pasos baja la tortuga? : "))
    avanzar(pasos_avance)
    bajar(pasos_bajada)

# AL FINAL, MUESTRO TODO EL RECORRIDO COMPLETO
print("\n\n=== RECORRIDO FINAL DE LA TORTUGA ===\n")
for linea in recorrido:
    print(linea)
```
