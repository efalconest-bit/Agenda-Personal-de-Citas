<h1 align="center"> AGENDA PERSONAL DE CITAS </h1>

El proyecto consiste en desarrollar una **aplicación de Agenda Personal de Citas**, que permita al usuario **registrar, consultar, modificar y eliminar citas** de manera rápida y organizada.  
El sistema busca facilitar la gestión del tiempo, evitando olvidos y mejorando la productividad personal o profesional.

## Objetivos
- Permitir al usuario administrar sus citas diarias, semanales o mensuales.
- Enviar recordatorios automáticos de las citas próximas.
- Facilitar la búsqueda de citas por fecha, tema o tipo.
- Garantizar que los datos sean seguros y se almacenen correctamente.

## Requerimientos no Funcionales
| ID | Tipo | Descripción |
|-|-|-|
| RNF1 | Usabilidad | La interfaz debe ser intuitiva y fácil de usar para usuarios no técnicos. |
| RNF2 | Rendimiento | El sistema debe cargar la agenda y las citas en menos de 3 segundos. |
| RNF3 | Seguridad de datos | Los datos de las citas deben mantenerse privados y protegidos. |
| RNF4 | Disponibilidad | La interfaz debe ser intuitiva y fácil de usar para usuarios no técnicos. | Los usuarios deben poder crear una cita en menos de 3 clics |
| RNF5 | Mantenibilidad | El sistema debe funcionar en diferentes dispositivos y navegadores. |

## Tabla de Prueba
| Nº | Requerimiento asociado | Datos de Entrada | Resultado esperado | Validacion |
|----|------------------------|------------------|--------------------|------------|
| 1. | RF1 – Registrar cita | Fecha: 15/11/2025<br>Hora: 09:00<br>Asunto: “Cita médica”<br>Descripción: “Chequeo general” | La cita se registra correctamente en la base de datos y se muestra en la lista de citas | Cita creada y visualizada correctamente en la agenda |
| 2. | RF2 – Consultar cita | Buscar: “médica” | El sistema muestra la cita registrada que contiene la palabra clave “médica” | Cita encontrada correctamente por palabra clave |
| 3. | RF3 – Editar cita | Cita seleccionada: “Cita médica”<br>Nuevo asunto: “Chequeo odontológico” | Se actualiza la cita con el nuevo asunto sin errores | Cita modificada correctamente y actualizada en pantalla |

## Propuesta de Mantenimiento
Se propone realizar un **mantenimiento evolutivo** para incorporar nuevas funcionalidades, como sincronización con Google Calendar o integración con asistentes virtuales.
También se planifica un **mantenimiento preventivo** mensual, enfocado en respaldos automáticos y actualizaciones de seguridad.

## Reflexión sobre el control de versiones
El uso de **Git** y **GitHub** permite mantener un control detallado sobre los cambios realizados en el sistema y en la documentación.  
Cada actualización se registra con fecha, autor y descripción, lo cual mejora la **colaboración**, la **organización** y la **transparencia del desarrollo**.  
Además, el control de versiones evita errores por sobrescritura de archivos y facilita la restauración de versiones anteriores si es necesario.

---

# Investigacion Sobre el Uso de **Markdown**

## ¿Qué es Markdown y por qué se utiliza en proyectos de software?
- **Markdown** es un lenguaje de marcado ligero que trata de conseguir la máxima legibilidad y facilidad de publicación tanto en su forma de entrada como de salida, inspirándose en muchas convenciones existentes para marcar mensajes de correo electrónico usando texto llano.
- Se utiliza en proyectos de software porque es fácil de leer, escribir y convierte el texto con formato a **HTML**, lo que lo hace ideal para documentación como archivos **README.md**, comentarios, blogs y portales de ayuda, ya que el código es más legible y fácil de mantener que el **HTML**. 

## Ejemplo de Como Usar Markdown
Esta seccion muestra cómo usar los **elementos básicos de formato** en **Markdown**:  
encabezados, listas, tablas, enlaces e imágenes.

### 1. Encabezados
Los encabezados se crean usando el símbolo **#**.  
Mientras más # uses, más pequeño será el título.

```
# Encabezado 1
## Encabezado 2
### Encabezado 3
```

### 2. Lista Desordenada
Se crea usando el simbolo **-** antes de una palabra.
```
- Palabra 1
- Palabra 2 
- Palabra 3
```

### 3. Lista Ordenada
Se crea usando numeros seguidos de un punto y un espacio.
```
1. Palabra uno
2. Palabra dos
3. Palabra tres
```

### 4. Tablas
Se crea usando tuberias **|** y guiones **-** rodeando el texto.
```
| Numero | Dato | Descripcion |
|--------|------|-------------|
| 1. | Uno | Primer numero |
| 2. | Dos | Segundo numero |
| 3. | Tres | Tercer numero |
```

### 5. Enlaces
Para crear un enlace se hace usando corchetes **[]** para el texto visible y paréntesis **()** para la URL.
```
[Texto del enlace](https://www.ejemplo.com)
```

### 6. Imagen 
Insertar imágenes es muy parecido a crear enlaces, pero se agrega un signo de exclamación **!** al inicio. La sintaxis es.
```
![Texto descriptivo](URL de la imagen)
```
Tambien se puede insertar simplemente arrastrando la imagen.

## Ventajas de utilizar **Markdown** en combinación con **GitHub**.
La combinación de **Markdown** y **GitHub** ofrece ventajas significativas como una escritura simplificada y enfocada, control de versiones de documentos, y la capacidad de crear documentación de proyectos completa y fácil de mantener. Esto permite a los desarrolladores colaborar eficientemente, documentar código de forma legible y rastrear cambios en la documentación o en notas, todo dentro del mismo entorno de trabajo. 
