# Tribute-page-vue

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
Tributo
Crea un nuevo proyecto con Vite

https://vuejs.org/guide/scaling-up/tooling.html#project-scaffolding
La idea es crear una página de tributo a algo que te guste, similar a este ejemplo. Dentro de este enlace, mira el "codepen" insertado. Tu página debe cumplir ciertos requisitos y vamos a acotar algunos componentes.

Iteración 1
Crea toda la página en App.vue. Tu aplicación debe cumplir todas las user stories indicadas en el enlace del ejemplo. Puedes pasar el juego de pruebas de las user stories añadiendo esta línea en el index.html . No te preocupes en exceso por los estilos, pero intenta que quede presentable. Puedes aprovechar algunos de los estilos que Vue trae por defecto o usar PicoCSS.

<script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>
Idealmente, tu página de tributo debería tener:

Título
Imagen con leyenda
Una lista de acontecimientos (lista desordenada)
Un enlace a una página externa
Iteración 2a
Usa la directiva v-for para crear tantos <li> como acontecimientos ocurren en tu págian de tributo. Puedes crear directamente un array de objetos en App.vue, o mejor, crea un fichero en formato JSON siguiendo la estrategia de Lab Ironhack Contacts
Recuerda añadir un identificador ficticio a cada objeto (un campo id). Será necesario para el v-for.
Iteración 2b
Vamos a dividir la página en componentes Podemos apreciar un par de componentes

ImageComponent
Este componente recibe dos propiedades (props).

El origen de datos de la imagne (URL a la imagen u objeto)
Leyenda de la imagen
Crea un ImageComponent.vue. Impórtalo desde App.vue y úsalo adecuadamente para emular el mismo comportamiento que tenía tu App hasta el momento.

BONUS
Reusa tu componente para añadir una segunda imagen al principio o final de tu lista de acontecimientos.

CronoList
Este componente recibe una propiedad (props)

¡Una array de objetos! A la propiedad le podemos llamar items . En este array, cada objeto, tiene dos propiedades, por ejemplo year y text.
Iteración 3
Divide el componente CronoList en dos componentes más pequeños

CronoItem
Este componente recibe dos propiedades (props)

year. Año en el que ha sucedido el acontecimiento
text. Texto describiendo el acontecimiento.
Ahora , CronoList debe importar CronoItem; y usarlo adecuadamente para crear tantos CronoItem como objetos recibe CronoList a través de la prop items

BONUS
Amplia la funcionalidad de la CronoList. Ahora, los objetos que recibe pueden tener una nueva propiedad de nombre isImportant. Indica que dicho acontecimiento es imporante o destacado. Destaca de alguna manera dichos elementos de la lista (un fondo de otro color, la letra más gruesa, etc.)

Piensa bien si esto es responsabilidad de CronoList o CronoItem

BONUS
Separa los estilos de los componentes. "Saca" los estilos de <style> en App.vue; y llévalos a cada componente gracias al uso de Scoped CSS

