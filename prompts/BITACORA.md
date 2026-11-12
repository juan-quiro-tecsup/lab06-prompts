
# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Alumno: JUAN CARLOS QUIRO ALVARO

Herramienta de IA usada: Claude

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. |34 |7 |
| The students program in Java. |29 |6 |
| desafortunadamente |18 |4 |

Conclusion: En el mismo chat la IA respondió bien porque el dato estaba en su ventana de contexto. Sin embargo, en el chat nuevo no lo sabía porque la ventana estaba vacía.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100 % | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3 % | BiblioTec, BiblioTec, LibroYa, LibroYa, LibroYa | 
| 1 | 44.5 % | PrestaLibro, BiblioTec, LibroYa, PrestaLibro, LibroYa |
| 1.8 | 32.2 % | BiblioTec, PrestaLibro, LibroYa, LibroYa, BiblioTec |

Conclusion: Al subir la temperatura, los porcentajes se reparten y los nombres varían más. Al ejecutar tres veces 1.8, los porcentajes fueron iguales pero los 5 intentos cambiaron cada vez. El simulador nunca inventa un nombre nuevo porque la temperatura solo cambia qué tan arriesgada es la elección entre las opciones que ya existen.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |SI |SI |
| Menciona a los usuarios principales |SI |SI |
| Tiene exactamente 3 funcionalidades |NO |SI |
| Esta en 3 parrafos |NO |SI |
| Lo usaria en un informe real |NO |SI |

Conclusion: Un prompr estructurado, te permite tener la informacion deseada con mayor puntualidad.

## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa en Java usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto | para gestionar los productos de una tienda. |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).|

- Nivel 1: La IA creó una calculadora en consola con operaciones básicas (sumar, restar, multiplicar y dividir). El pedido era tan general que eligió un programa cualquiera, sin relación con lo que yo necesitaba.
- Nivel 2: La IA siguió creando un programa genérico, pero el código salió más ordenado: con comentarios, métodos separados y una breve explicación de cómo compilarlo y ejecutarlo. El rol cambió el estilo, no el tema.
- Nivel 3: La IA ya entendió que el programa era para una tienda y creó un sistema para gestionar productos con un menú en consola (agregar, listar, buscar y eliminar). Los atributos de los productos los inventó ella, por ejemplo id, nombre, precio y cantidad.
- Nivel 4: La IA creó la clase Producto con exactamente los atributos que pedí: codigo, nombre, precio y stock, con su constructor y sus getters y setters, y organizó el programa alrededor de esa clase.
- Nivel 5: La IA creó un sistema para gestionar los productos de una tienda y empezó explicando la estructura de la clase antes de presentar el código Java, en el orden que pedí. Los métodos siguieron el estilo indicado, getPrecio() y setPrecio(double precio).