1. Explicar cuantas maneras existen para vincular html con css
  - Existen 4 tipos:
    - En linea: esta vinculación es cuando se coloca los estilos en la misma etiqueta html.
    ```html
    <p style="color:red;">test</p>
    ```
    - En bloque: esta vinculación es cuando se genera estilos utilizando la etiqueta style dentro del html.
    ```html
    <style>
      p {
        color: red;
      }
    </style>
    ```
    - Externa: esta vinculación es cuando se utiliza la etiqueta link y se llama el archivo .css
    ```html
    <link rel="stylesheet" href="style.css"/>
    ```
    - Import: esta vinculación es cuando se utiliza la regla @import de css en un bloque o archivo css
    ```css
    @import url("style.css");
    ```
2. Explicar con sus palabras el conjunto de reglas de css (selector, propiedad, valor)
  - selector: un selector nos ayuda a poder seleccionar o conectar el css a una etiqueta html.
  ```css
    selector{}
  ```
  - propiedad: una propiedad nos ayuda a poder modificar una caracteristica como el color, tamaño, sombras, margenes, altura, anchos, etc.
  ```css
    selector{
      propiedad:
    }
  ```
  - valor: el valor es la cantidad o tipo que se va a configurar en la propiedad pueden ir numeros, letras depende de la propiedad que se utilice.
  ```css
    selector{
      propiedad: valor;
    }
  ```
3. Explicar los 4 conceptos importantes con ejemplos (selectores, herencia, cascada, especificidad)
  - selectores: existen varios tipos de selectores:
    - por elemento: este ayuda a seleccionar por tipo de etiqueta.
    ```css
    p{}
    ```
    - por clase: este ayuda a seleccionar varias etiquetas que contengan la clase indicada.
    ```css
    .parrafo{}
    ```
    - por id: este ayuda a seleccionar una sola etiqueta identificada por un id.
    ```css
    #parrafo{}
    ```
    - universal: este ayuda a seleccionar todos los elementos del html.
    ```css
    *{}
    ```
    - por decendencia: este ayuda a seleccionar los hijos de un elemento.
    ```css
    div p{}
    ```
    - por atributo: este ayuda a seleccionar etiquetas con atributos especificos de esta.
    ```css
    input[type="text"]{}
    ```
    - por pseudo-clase: este ayuda a seleccionar etiquetas con estados especificos.
    ```css
    button:hover{}
    ```
    - por pseudo-elemento: este ayuda a seleccionar partes especificar de un elemento.
    ```css
    p::after{}
    ```
  - herencia: son los estilos que las etiquetas hijas heredan del padre.
    - para este ejemplo la etiqueta h1 va a heredar el color y la fuente de body.
    ```css
    body{
      font-family: Arial, sans-serif;
      color: red;
    }
    h1 {
      font-size: 16px
    }
    ```
  - cascada: los estilos siguen un patron de cascada cada propiedad que se ponga abajo de otra sera la que va a tener prioridad ante otras.
    - en este ejemplo el color sera rojo porque es el ultimo en la cascada.
    ```css
    body{
      background-color: blue;
    }
    p{
      background-color: red;
    }
    ```
  - especificidad: es una medida de que tan especifica puede ser una regla para el elemento donde se suma todo lo anterior mencionado, la cascada, selectores,orden, etc.
    - para este ejemplo el color sera rojo porque se especifica con !important el cual es la mayor especificidad posible en css.
    ```css
    body{
      color: blue
    }
    p{
      color: red !important;
    }
    ```