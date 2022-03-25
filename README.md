# The Cocktail Proyect

En este proyecto se realiza la creación de dos tabs maquetados y desarrollados con Vue.JS 

## Comenzando 🚀

Para ejecutar el código de este proyecto es necesario: 

### Instalar las dependencias 🔧

```
npm install
```

## Compilar en caliente 🔥

```
npm run serve
```

## Compila y minifica para la producción

```
npm run build
```

## Ejecutando las pruebas ⚙️

- Ejecución correcta del proyecto.
- Visual igual que en Figma del Tab_1.
    - Altura correcta de los régimenes en la Tab_1.
    - **Clicar en cualquier parte** del régimen para que se active la opción.
    - Color del borde y del input correcta al estar activado/desactivado.
    - Transición al hacer hover sobre un régimen (**sombreado**).
    - Transición al clicar en un régimen (**border-radius y border-color**).
    - Responsive:
        - Al achicar la pantalla los régimenes tienen un scroll para que no se rompan.
        - Al llegar a 768px, se cambia a 2 columnas y el texto principal de HOTEL Mieres del Camín Apartamentos se centra.
        - Al llegar a 360px, se cambia a 1 columna.
- Visual igual que en Figma del Tab_3.
    - Se introduce **scroll únicamente en los paneles de las cervezas**, lo demás es fijo.
    - Visualización siempre del paginador.
    - Correcta **funcionalidad del paginador** al moverse por las distintas páginas.
    - Correcta visualización de los **food_pairing**.
    - Responsive: 
        - Al achicar la pantalla el texto de las cervezas se van colapsando. En el caso de que el texto sea muy grande, sigue creciendo el panel pero sigue centrada la imagen y la abv arriba a la derecha.
        - Al llegar a 360px, **se cambia la disposición del panel a filas**: primero la **imagen**, después el **nombre y descripción** y finalizando por la **abv**.
- [Animación]: transición en el color de los tabs superiores.
- **Totalmente responsive**.
- **Accesible**.
- **Escalable** si se añaden más hijos.
- Estructura del proyecto adecuada.


## Construido con 🛠️

* [VueCli](https://cli.vuejs.org/)
* [Vue3](https://vuejs.org/)
* [SCSS] - Maquetación 

## Autor ✒️

* **Miguel González** - [miguegonzalez](https://github.com/miguegonzalez)

### Personalización de la configuración
Ver [Configuration Reference](https://cli.vuejs.org/config/).
