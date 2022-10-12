![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | Vue.js IronContacts

## Introducción

Después de Ironhack, has decidido trabajar en la industria del cine, y has encontrado un trabajo en el que necesitas gestionar los contactos de un famoso productor.

Tu tarea es crear una aplicación de gestión de contactos para el productor utilizando Vue.js.

## Configuración

- Haz un fork de este repo
- Clona este repositorio
- Abre el LAB y comienza:

  ```bash
  $ cd lab-vue-ironcontacts-es
  $ yarn
  $ yarn dev
  ```

## La presentación

- Al terminar, ejecuta los siguientes comandos:

  ```bash
  git add .
  git commit -m "done"
  git push origin main
  ```

- Crea un Pull Request para que tus TAs puedan comprobar tu trabajo.

## Instrucciones

### Iteración 1 | Mostrar 5 contactos

Echemos un vistazo al código de inicio.

Dentro de la carpeta `src/data` tenemos un archivo `contacts.json` que contiene los contactos del productor. Importa el archivo `contacts.json` a `App.vue`. Una vez hecho esto, crea una variable ref llamada `contacts` y almacena un **array que contenga los 5 primeros contactos**.

Muestra ese array de 5 contactos como una lista en una `<table>` y muestra la `picture`, el `name` y la `popularity` de cada contacto.

Por ahora, vamos a renderizar el contenido en `App.vue`. Dicho esto, no procedas a crear un componente dedicado para la lista de contactos. La razón será un poco más clara más tarde cuando añadamos el botón de eliminar junto a cada contacto. Probablemente aún no estés familiarizado con el concepto de "levantar el estado" y pasar callbacks como props. Por esta razón, es mejor renderizar todo en un solo componente por el momento.

Procedamos.

Para importar `contacts.json` en `App.vue`, puedes usar

```js
import contacts from "./data/contacts.json";
```

Al final de esta iteración, tu aplicación debería tener este aspecto:

<details>
  <summary> Comprobar imagen dentro - Iteración 1</summary>

![Screenshot - Iteration 1](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-1.png)

</details>

### Iteración 2 | Mostrar condicionalmente la información de los premios

El productor quiere ver la información sobre los _premios_ que ha ganado el contacto.

Actualiza la lista y añade dos columnas más "Ganó un Oscar" y "Ganó un Emmy", al final de la tabla. A continuación, en función del valor `wonOscar` y `wonEmmy` de cada contacto, renderiza condicionalmente un icono de trofeo :trophy: o ningún contenido.

Una vez hecho esto, tu aplicación debería tener este aspecto:

<details>

<summary> Comprobar imagen dentro - Iteración 2</summary>

![Screenshot - Iteration 2](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-2.png)

</details>

### Iteración 3 | Añadir nuevos contactos aleatorios

En su aplicación, cree un botón de Añadir Contacto _Aleatorio_. Cada vez que hagas clic en este botón, debería añadir un nuevo contacto aleatorio a los `contactos`. Deberías obtener contactos aleatorios de los contactos restantes que aún no se muestran.

Primero, selecciona al azar un contacto de la matriz de contactos restantes. A continuación, añade ese contacto a la array que vive en tu ref de datos (que es la array creada anteriormente de 5 contactos).

Al final de esta iteración, su sitio web probablemente se verá así:

<details>
  <summary> Ver imagen interior - Iteración 3 </summary>

![Screenshot - Iteration 3](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-3.png)

</details>

### Iteración 4 | Ordenar los contactos por nombre y popularidad

El productor le ha pedido que añada dos nuevos botones para ayudarle a ordenar sus contactos. Al hacer clic en uno de los botones, debería **ordenar la tabla por `name`** (alfabéticamente), y al hacer clic en el otro, debería ordenar por **popularidad** (la más alta primero).

Una vez que hayas ordenado la matriz, recuerda actualizar la variable de estado que contiene los contactos.

Esto es lo que deberías tener al final de esta iteración:

<details>
  <summary> Comprobar imagen interior - Iteración 4 </summary>

![Screenshot - Iteration 4](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-4.png)

</details>

### Iteración 5 | Eliminar contactos

El productor también quiere eliminar algunos de sus contactos. Implementar un botón de _delete_ en cada fila de su `<table> ` que permitirá al usuario eliminar el contacto que hizo clic.

Cuando hagan clic, deberás obtener el `id` de ese actor y utilizarlo para eliminar el contacto del array. Recuerda actualizar la variable de estado que contiene los contactos después de eliminar el contacto.

Una vez hecho esto, tu aplicación debería tener este aspecto (después de jugar un poco con el botón _Delete_ ):

<details>
  <summary> Ver imagen interior - Iteración 5 </summary>

![Screenshot - Iteration 5](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-5.png)

</details>

### Iteración 6 | Bono | Estilo

Desafortunadamente, esta lista de contactos no está lista para la producción. Estamos en el negocio del cine. Tiene que brillar. Añade algo de CSS para que la aplicación sea más atractiva.

<br/>

Feliz codificación! :blue_heart: