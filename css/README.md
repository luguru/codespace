# Proyecto CodeSpace

## Descripción
**ITCSS (Inverted Triangle CSS)** es una metodología de organización de hojas de estilo CSS que se basa en una estructura de pirámide invertida para garantizar una gestión eficiente de los estilos y evitar problemas de especificidad y cascada en CSS. Fue propuesta por Harry Roberts y se utiliza para mantener un código CSS más mantenible y escalable. La estructura ITCSS consta de varias capas o niveles que se organizan de manera descendente en cuanto a especificidad y alcance.
La idea principal detrás de ITCSS es que los estilos se vuelven más específicos a medida que desciendes por la pirámide. Esto ayuda a evitar conflictos de cascada y facilita la comprensión y el mantenimiento del código CSS. Al seguir esta estructura, se promueve la reutilización de estilos y se reduce la necesidad de anular reglas de estilo existentes.

## Uso
### **Settings (Configuración):**
En la parte superior de la pirámide invertida, se encuentran las variables y configuraciones globales. Estos pueden incluir colores, fuentes, tamaños de texto y otras configuraciones globales utilizadas en todo el proyecto.

### **Tools (Herramientas):**
Esta capa contiene las utilidades y funciones de Sass (u otro preprocesador CSS) que se utilizan en todo el proyecto. Aquí se definen mixins, funciones, variables y clases reutilizables que no generan estilos directamente, pero que se utilizan para construir estilos en capas posteriores.

### **Generic (Genérico):**
En esta capa, se establecen los estilos CSS genéricos que afectan a elementos HTML no específicos, como estilos de reinicio (reset), normalización (normalize), estilos para etiquetas HTML básicas, etc. Estos estilos proporcionan una base coherente para el proyecto.

### **Elements (Elementos):**
En esta capa, se definen estilos para elementos HTML específicos, como encabezados (`<h1>`, `<h2>`, etc.), párrafos (`<p>`), enlaces (`<a>`), botones, etc. Estos estilos son de baja especificidad y se aplican a elementos HTML sin clases o identificadores específicos.

### **Objects (Objetos):**
En esta capa, se crean clases y estilos reutilizables que representan componentes o elementos de diseño que se utilizan en todo el sitio, como un sistema de cuadrícula, botones personalizados o formularios. Los estilos en esta capa pueden ser más específicos que los de las capas anteriores.

### **Components (Componentes):**
Aquí se definen estilos para componentes específicos de la interfaz de usuario. Los estilos son más específicos y se aplican a elementos con clases específicas que representan componentes reutilizables, como encabezados personalizados, tarjetas, barras de navegación, etc.

### **Trumps (Triunfos):**
En la parte inferior de la pirámide invertida, se encuentran los estilos de alta especificidad, como clases de utilidad. Estos estilos anulan cualquier estilo anterior y se utilizan para realizar ajustes finos o corregir problemas específicos de diseño.

### Style.css
Finalmente se crea un archivo en la raíz llamado styles.css o main.css donde se importan todos los archivos creados anteriormente, en el orden establecido para mantener la especificidad y cascada de css.
