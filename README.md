<h1 align="center"> AGENDA PERSONAL DE CITAS </h1>

## Descripción del Sistema 
La Agenda Personal de Citas es una aplicación diseñada para registrar, organizar y 
gestionar citas personales o profesionales. Permite al usuario agendar nuevas citas, editar 
o eliminar existentes, visualizar por día/semana/mes y recibir recordatorios. Su objetivo 
es facilitar la organización del tiempo y evitar olvidos, siendo útil para profesionales o 
estudiantes. 

## Objetivos
- Permitir al usuario administrar sus citas diarias, semanales o mensuales.
- Enviar recordatorios automáticos de las citas próximas.
- Facilitar la búsqueda de citas por fecha, tema o tipo.
- Garantizar que los datos sean seguros y se almacenen correctamente.

## Requerimientos Funcionales
Son los que describen qué debe hacer el sistema.
Definen las funcionalidades, acciones o servicios que la aplicación debe ofrecer.
| **Código** | **Descripción** | **Criterio de Éxito** |
|------------|------------------|------------------------|
| **RF-01: Gestión de Citas** | El sistema debe permitir al usuario crear, visualizar, modificar y eliminar citas. | Para cada cita, el usuario debe poder almacenar como mínimo: título, fecha, hora, ubicación y descripción. |
| **RF-02: Búsqueda y Filtrado** | El sistema debe permitir al usuario buscar citas por título o descripción, y filtrar la lista de citas por fecha o etiquetas. | El usuario debe obtener una lista de citas que coincidan con el término de búsqueda o los criterios de filtrado aplicados. |
| **RF-03: Categorización con Etiquetas** | El sistema debe permitir asignar una o múltiples etiquetas personalizadas a cada cita. | El usuario puede crear nuevas etiquetas y asignarlas a cualquier cita durante su creación o edición. |
| **RF-04: Notificaciones y Recordatorios** | El sistema debe permitir al usuario configurar recordatorios para cada cita. | El sistema mostrará una notificación visual o sonora en el momento programado. |
| **RF-05: Respaldo y Sincronización** | El sistema debe permitir respaldar y restaurar toda la información de la agenda. | El archivo de respaldo contendrá toda la información de citas y etiquetas y permitirá recuperar los datos en otro dispositivo. |

## Requerimientos no Funcionales
Describen cómo debe comportarse el sistema, pero no son funciones directas.
Tienen que ver con la calidad, rendimiento, seguridad, usabilidad, etc.
| Código RNF | Nombre del Requerimiento           | Descripción                                                                                                                  |
|------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| RNF-01     | Rendimiento (Capacidad de Respuesta) | La interfaz debe ser responsive y todas las operaciones (agregar, editar o buscar una cita) deben ejecutarse en menos de 2 segundos. |
| RNF-02     | Usabilidad                         | La interfaz debe ser intuitiva y fácil de usar; un usuario nuevo debe poder agregar su primera cita en menos de 3 minutos sin consultar un manual. |
| RNF-03     | Seguridad y Privacidad             | Los datos deben estar protegidos; las contraseñas deben almacenarse encriptadas y la base de datos local no debe ser accesible sin permisos. |


## Tabla de Prueba
| Caso de Prueba                | Requerimiento Asociado | Datos de Entrada                                                                                      | Resultado Esperado                                                                                       | Resultado Obtenido                           |
|------------------------------|--------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| CPU-01: Creación de cita válida | RF-01: Gestión de Citas   | Título: "Reunión médico", Fecha: "2024-06-15", Hora: "10:00"                                           | Sistema crea la cita exitosamente y la muestra en la lista                                                | ✔ PASA - Cita creada correctamente            |
| CPU-02: Búsqueda por título existente | RF-02: Búsqueda y Filtrado | Término: "dentista" (con citas: "Limpieza dental", "Reunión trabajo")                                   | Retorna 2 citas con "dentista" en título o descripción                                                     | ✔ PASA - Encontró 2 citas correctamente       |
| CPU-03: Asignación de etiqueta múltiple | RF-03: Categorización y Etiquetas | Cita: "Entrega proyecto", Etiquetas: ["Trabajo", "Urgente"]                                            | Asigna las 2 etiquetas y las muestra en la interfaz                                                       | ✔ PASA - Etiquetas asignadas correctamente    |

## Pruebas de Validación
| Prueba de Validación                  | Requerimiento Asociado     | Datos de Entrada                                                                                      | Resultado Esperado                                                                                  | Resultado Obtenido                                   |
|---------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| CPV-01: Flujo completo de recordatorio | RF-04: Notificaciones y Recordatorios | Cita con recordatorio para *2024-06-10 18:00*                                                          | Muestra notificación en fecha y hora programadas                                                    | ✔ PASA - Recordatorio activado correctamente          |
| CPV-02: Respaldo e integridad de datos | RF-05: Respaldo y Restauración | Agenda con 15 citas y 5 etiquetas. Exportar → Eliminar → Importar                                      | Restaura todos los datos exactamente igual                                                          | ✔ PASA - Todos los datos recuperados sin pérdida      |


## Propuesta de Mantenimiento
Se propone realizar un mantenimiento continuo de la Agenda Personal de Citas para garantizar su correcto funcionamiento, adaptarse a los futuros cambios tecnológicos y mejorar la experiencia del usuario. Este mantenimiento permitirá corregir fallos, optimizar el rendimiento y mantener la aplicación estable, segura y eficiente a lo largo del tiempo.

## Reflexión sobre el control de versiones
El control de versiones en GitHub permite llevar un historial claro de los cambios, recuperar archivos si ocurre un error y trabajar de forma más organizada. Es una herramienta esencial para mantener la documentación y el desarrollo seguros, ordenados y fáciles de gestionar. 

---


# Investigacion Sobre el Uso de **Markdown**

## ¿Qué es Markdown y por qué se utiliza en proyectos de software?
- **Markdown** es un lenguaje de marcado ligero diseñado para permitir la creación de documentos de texto formateado utilizando una sintaxis sencilla y fácil de leer. Su objetivo principal es facilitar la escritura de documentación sin depender de herramientas complejas o interfaces gráficas. 

## En proyectos de software, Markdown se utiliza ampliamente debido a: 
| Ventaja                 | Descripción                                                                                           |
|-------------------------|--------------------------------------------------------------------------------------------------------|
| Simplicidad y legibilidad | Permite escribir documentos claros sin distraerse con el formato.                                      |
| Compatibilidad            | Es soportado por múltiples plataformas, editores y sistemas de control de versiones.                   |
| Versatilidad              | Puede usarse para crear README, especificaciones técnicas, documentación de APIs, wikis y más.         |
| Conversión sencilla       | Puede transformarse fácilmente en HTML, PDF u otros formatos.                                          |
| Integración con GitHub    | GitHub procesa automáticamente archivos `.md`, permitiendo mostrar documentación de manera clara en línea. |

## Ejemplo de Como Usar Markdown
Esta seccion muestra cómo usar los **elementos básicos de formato** en Markdown:  
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
| Ventaja                   | Descripción                                                                                                  |
|---------------------------|---------------------------------------------------------------------------------------------------------------|
| Documentación clara y estandarizada | Facilita la creación de archivos como README.md o manuales técnicos.                                         |
| Control de versiones      | Todos los cambios quedan registrados, permitiendo rastrear modificaciones en la documentación.                |
| Colaboración eficiente    | Varios usuarios pueden editar, revisar o comentar la documentación usando pull requests.                     |
| Visualización inmediata   | GitHub renderiza automáticamente el Markdown, mostrando el documento con formato adecuado.                   |
| Portabilidad              | Los archivos `.md` son livianos y funcionan en cualquier sistema operativo.                                  |
 
