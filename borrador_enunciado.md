# Pregunta X: DDCampeonato: Liga Neo-Computista ⚽

## Introducción

Durante las vacaciones decidiste descancar y explorar nuevas cosas, ahí descubriste el manga de *Blue lock*, fue tal tu gusto por el manga que apenas volviste de vacaciones decidiste llegar al DCC y proponer hacer un campeonato, como en el DCC todos son otakus aceptaron la idea gustosos, y así nació el **DDCampeonato: Liga Neo-Computista**.
Lamentablemente como tú fuiste el de la idea te tocó organizar el campeonato, así que decides partir creando una función para obtener los partidos siguientes de un equipo, teniendo en cuenta que todos los equipos deben jugar contra todos 1 vez (igual que en la liga Neo-egoísta).

## Objetivo

Tu objetivo es definir la función `obtener_proximos` la cual recibe `partidos`, una lista de listas que esta compuesta por listas de la forma `["nombre_equipo_X", "nombre_equipo_Y"]`, también recibe un *string* `equipo` el cual es el nombre del equipo a revisar.
La función debe retornar una lista con todos los equipos con los que aún no juega.

El *input* será automaticamente recibido, por lo que tu única tarea es definir la función `obtener_proximos(partidos, equipo)`. De igual manera la primera fila linea será una lista de listas de partidos, la segunda linea será un *string*, y en la tercera linea se llamará a la función ocupando como parametros las dos primeras lineas y en la cuarta linea se imprimira la lista de equipos.

## Ejemplos

### Ejemplo 1

**Input**
```python
partidos = [["Bastard Munchen", "FC Barcha"],
            ["PXG", "Ubers"],
            ["Bastard Munchen", "Manshine City"],
            ["PXG", "FC Barcha"],
            ["Bastard Munchen", "Ubers"]]
equipo = "Bastard Munchen"
resultado = obtener_proximos(partidos, equipo)
print(resultado)
```

**Output**
```python
["PXG"]
```

**Explicación**: Los 5 equipos presentes en el campeonato son `"Bastard Munchen"`, `"FC Barcha"`, `"PXG"`, `"Manshine City"`y `"Ubers"`, el equipo el cual nos piden revisar es `"Bastard Munchen"` si vemos la lista de partidos `"Bastard Munchen"` ha jugado partidos contra todos los equipos menos contra el `"PXG"` por tanto la función retorna `["PXG"]`

### Ejemplo 2

**Input**
```python
partidos = [["Team Z", "Team X"],
            ["Team Z", "Team Y"],
            ["Team Z", "Team W"],
            ["Team Z", "Team V"]]
equipo = "Team Z"
resultado = obtener_proximos(partidos, equipo)
print(resultado)
```

**Output**
```python
[]
```
**Explicación**: Los 5 equipos presentes en el campeonato son `"Team Z"`, `"Team X"`, `"Team Y"`, `"Team W"`, `"Team V"`, el equipo el cual vamos a revisar es el `"Team Z"`, revisando la lista de partidos `"Team Z"` ha jugado partidos contra todos los equipos del campeonato por lo que la función debe retornar una lista vacía, ya que no tiene equipos pendientes contra los que jugar.

## Testcases