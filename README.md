# The Cocktail Proyect

En este proyecto se realiza la creaci贸n de dos tabs maquetados y desarrollados con Vue.JS 

## Comenzando 馃殌

Para ejecutar el c贸digo de este proyecto es necesario: 

### Instalar las dependencias 馃敡

```
npm install
```

## Compilar en caliente 馃敟

```
npm run serve
```

## Compila y minifica para la producci贸n

```
npm run build
```

## Ejecutando las pruebas 鈿欙笍

- Ejecuci贸n correcta del proyecto.
- Visual igual que en Figma del Tab_1.
    - Altura correcta de los r茅gimenes en la Tab_1.
    - **Clicar en cualquier parte** del r茅gimen para que se active la opci贸n.
    - Color del borde y del input correcta al estar activado/desactivado.
    - Transici贸n al hacer hover sobre un r茅gimen (**sombreado**).
    - Transici贸n al clicar en un r茅gimen (**border-radius y border-color**).
    - Responsive:
        - Al achicar la pantalla los r茅gimenes tienen un scroll para que no se rompan.
        - Al llegar a 768px, se cambia a 2 columnas y el texto principal de HOTEL Mieres del Cam铆n Apartamentos se centra.
        - Al llegar a 360px, se cambia a 1 columna.
- Visual igual que en Figma del Tab_3.
    - Se introduce **scroll 煤nicamente en los paneles de las cervezas**, lo dem谩s es fijo.
    - Visualizaci贸n siempre del paginador.
    - Correcta **funcionalidad del paginador** al moverse por las distintas p谩ginas.
    - Correcta visualizaci贸n de los **food_pairing**.
    - Responsive: 
        - Al achicar la pantalla el texto de las cervezas se van colapsando. En el caso de que el texto sea muy grande, sigue creciendo el panel pero sigue centrada la imagen y la abv arriba a la derecha.
        - Al llegar a 360px, **se cambia la disposici贸n del panel a filas**: primero la **imagen**, despu茅s el **nombre y descripci贸n** y finalizando por la **abv**.
- [Animaci贸n]: transici贸n en el color de los tabs superiores.
- **Totalmente responsive**.
- **Accesible**.
- **Escalable** si se a帽aden m谩s hijos.
- Estructura del proyecto adecuada.


## Construido con 馃洜锔?

* [VueCli](https://cli.vuejs.org/)
* [Vue3](https://vuejs.org/)
* [SCSS] - Maquetaci贸n 

## Autor 鉁掞笍

* **Miguel Gonz谩lez** - [miguegonzalez](https://github.com/miguegonzalez)

### Personalizaci贸n de la configuraci贸n
Ver [Configuration Reference](https://cli.vuejs.org/config/).
