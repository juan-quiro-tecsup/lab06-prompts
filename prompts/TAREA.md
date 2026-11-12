# Tarea: Mi prompt profesional

## Funcionalidad elegida

Registro de clientes de una tienda en Java (programa de consola para agregar, listar y buscar clientes).

## Version 1: prompt basico

```text
Crea un registro de clientes en Java.
```


La IA creo un programa simple con una clase Cliente y una lista, pero eligio por su cuenta los atributos (por ejemplo nombre, telefono y email), no indico nada sobre el formato ni sobre como explicar el codigo.

## Version 2

```text
Actua como desarrollador Java. Crea un registro de clientes en Java para una tienda, con una clase Cliente que tenga los atributos codigo, nombre y correo.
```

Que mejoro: la clase Cliente ya uso los atributos codigo, nombre y correo, y el codigo salio mas ordenado. Todavia faltaba controlar que hacia el programa, no dije que librerias usar ni como presentar la respuesta, y la explicacion no venia en un orden claro.

## Version 3: prompt final

```text
Actua como desarrollador Java. Crea un programa de consola para registrar clientes de una tienda, donde se pueda agregar, listar y buscar clientes por codigo. Usa una clase Cliente con los atributos codigo, nombre y correo, y guarda los clientes en un ArrayList. No uses librerias externas ni bases de datos. Usa este estilo para los metodos: getNombre(), setNombre(String nombre). Explica primero la estructura de la clase y luego presenta el codigo Java en un solo bloque.
```

Que mejoro: la IA explico primero la estructura de las clases Cliente y TiendaClientes y despues presento el codigo. Creo un menu con agregar, listar, buscar por codigo y salir, uso solo ArrayList y Scanner (que vienen incluidos en Java) y siguio el estilo de metodos pedido (getNombre(), setNombre(String nombre)).

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa de consola para registrar clientes de una tienda, donde se pueda agregar, listar y buscar clientes por codigo. |
| Contexto | Usa una clase Cliente con los atributos codigo, nombre y correo, y guarda los clientes en un ArrayList. |
| Restriccion | No uses librerias externas ni bases de datos. |
| Ejemplo | Usa este estilo para los metodos: getNombre(), setNombre(String nombre). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java en un solo bloque. |

## Evaluacion del resultado

| Criterio | Cumple |
|----------|--------|
| Explica la estructura antes del codigo | Si |
| Usa la clase Cliente con codigo, nombre y correo | Si |
| Guarda los clientes en un ArrayList | Si |
| No usa librerias externas | Si |
| Usa el estilo getNombre() y setNombre(String nombre) | Si |
| El codigo esta en un solo bloque | Si |

## Errores que evite

- En la v1 el pedido era muy vago. En la v3 indique que el programa debe agregar, listar y buscar clientes por codigo.
- En la v3 pedi explicar primero la estructura de la clase y luego el codigo en un solo bloque, asi la respuesta salio en el orden que queria.