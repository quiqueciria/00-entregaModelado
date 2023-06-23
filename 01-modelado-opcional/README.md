# 01-entrega-modelado

## Caso opcional

**Tener un sólo nivel de áreas es limitado, lo suyo sería tener una estructura jerárquica,**
He sustituido la anterior colección de _tematicas_ por una nueva pensando en las áreas. Dentro de cada área tenemos un array que nos devuelve:

- idTecnologia
- Nombre
- Descripción

A la vez dentro de cada tecnología podemos ver los vídeos contenidos, que hacen referencia a la colección _videos_.

![](./content/Screenshot%202023-06-23%20at%2013.22.19.png)

---> En la colección paginaPrincipal he creado un objeto _areaDestacada_ que podría llamar a cada área (_tematicas_) y nos devolvería los vídeos más destacada de cada área.

![](./content/Screenshot%202023-06-23%20at%2013.23.01.png)

**Van a haber videos públicos y privados, es decir:
Un curso puede ser 100% público.**
He introducido un booleano para preguntar si un curso es público o no.

**Un curso puede tener una parte inicial 100% pública, y otra sólo para subscriptores.**
En este caso he introducido otro _booleano_ para saber si un video es público o no.

![](./content/Screenshot%202023-06-23%20at%2013.23.44.png)

**Esto implica que hayan usuarios registrados y subscripciones**
He creado una nueva colección que contendría los usuarios y se preguntaría si es _dePago_ o no.

![](./content/Screenshot%202023-06-23%20at%2013.24.12.png)

⚠️ Hemos visto si un vídeo o curso es público o no; pero no me queda claro, si es público para usuarios registrado solo o cualquiera (aunque no esté registrado) que entre en la página. Ahora creo que hay tres tipos de usuarios:

- Usuario no registrado (visita la página)
- Usuario registrado (puede ser de pago o no)
- Usuario subscrictor
