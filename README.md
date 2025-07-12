# RETO 8 👽

## Ejercicio 3
- Escriba una función recursiva para calcular la operación de la potencia.
```python
# Definimos una función recursiva que calcula la potencia de un número entero
def exp_recur(num: int, exp: int) -> int:
    # Caso base: cualquier número elevado a 0 es 1
    if exp == 0:
        return 1
    # Si el número base es 0 y el exponente no es 0, el resultado es 0
    elif num == 0:
        return 0
    else:
        # Paso recursivo: multiplicamos el número por el resultado de llamarse a sí misma
        # con el exponente reducido en 1
        return num * exp_recur(num, exp - 1)

# Punto de entrada del programa
if __name__ == "__main__":
    # Solicitamos al usuario que ingrese la base (num)
    num = int(input("Ingrese un numero: "))
    
    # Solicitamos al usuario que ingrese el exponente (exp)
    exp = int(input("Ingrese un exponente: "))
    
    # Calculamos la potencia usando la función recursiva
    potencia = exp_recur(num, exp)
    
    # Mostramos el resultado al usuario
    print(f"La potencia de {num} a la {exp} es: {potencia}")

```
**Diagrama de Flujo**
``` mermaid
---
config:
  theme: redux
---
graph TD
    A[Inicio] --> B[Ingresar num]
    B --> C[Ingresar exp]
    C --> D[Llamar funcion 'potencia_recur num exp']
    D --> E{exp == 0}
    E -- Sí --> F[return 1]
    E -- No --> G{num == 0}
    G -- Sí --> H[return 0]
    G -- No --> I[return num * potencia_recur num exp - 1] 
    --> D

```

# Autor 🤖
- [Juan Carlos Polania Bolivar](https://github.com/Ciyuang)
