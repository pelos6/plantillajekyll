---
layout: default
title: chuleta markdown
---
[inicio](index.html)  / [programacion](programacion.html) / [markdwon](markdown.html) / markdown Chuleta 
<!-- MarkdownTOC -->

- [parrafos y saltos de linea](#parrafos-y-saltos-de-linea)
- [texto no interpretado](#texto-no-interpretado)
- [listas de tareas](#listas-de-tareas)
- [cabeceras](#cabeceras)
- [simulando un H1  para cabeceras grandes](#simulando-un-h1--para-cabeceras-grandes)
        - [simulando un H6  para cabeceras pequeñas](#simulando-un-h6--para-cabeceras-pequeñas)
- [enlaces](#enlaces)
- [codigo](#codigo)
- [Identificadores de Cabecera](#identificadores-de-cabecera)
    - [Esto es una cabecera con un Id](#cabecera1)
- [listas](#listas)
- [imagenes](#imagenes)
- [tablas](#tablas)
- [otras chuletas](#otras-chuletas)
- [enlaces de interes](#enlaces-de-interes)

<!-- /MarkdownTOC -->

# parrafos y saltos de linea
- Para crear párrafos se deja una línea en blanco.

- Para crear un salto de línea dentro de un párrafo,   
ademas del salto es necesario poner dos  
espacios al final de la última palabra de esa línea  
- para escapar caracteres especiales se usa  \

# texto no interpretado

con acentos invertidos.  
\```

``` 
para texto que no se interpreta 
```

# listas de tareas  
pero no funciona ...  
- [x] Finish my changes  
- [ ] Push my commits to GitHub  
- [ ] Open a pull request  

# cabeceras

pueden simular los tags h de html

# simulando un H1  para cabeceras grandes 

```
# H1  para cabeceras grandes 
```

###### simulando un H6  para cabeceras pequeñas 

```
###### H6  para cabeceras grandes 
```

# enlaces 

```
a una url
[chuleta de Markdown](http://joedicastro.com/pages/markdown.html)
```

[chuleta de Markdown](http://joedicastro.com/pages/markdown.html)

# codigo
pero no parece funcionar

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

# Identificadores de Cabecera
Los identificadores de cabecera nos permiten establecer un Identificador a las cabeceras para luego poder enlazarlas en cualquier otro lugar del texto. Es lo que empleo para crear el índice de esta página. Funcionaría como un anchor HTML (ancla) pero que solo se puede aplicar en las cabeceras.  

### Esto es una cabecera con un Id {#cabecera1}

[Enlace a esa cabecera](#cabecera1)

# listas
```
Lista numerada (ordenada)

1. Este es el primer elemento
2. Este es el segundo elemento
3. Este es el tercer elemento

Lista de puntos (desordenada)

* Un elemento de la lista
y su texto
* Otro elemento de la lista
* El tercer elemento de la lista
```


1. Este es el primer elemento
2. Este es el segundo elemento
3. Este es el tercer elemento

* Un elemento de la lista  
y su texto
* Otro elemento de la lista
* El tercer elemento de la lista


# imagenes
La manera de enlazar imágenes es básicamente la misma de crear enlaces, con un única diferencia, se añade el carácter exclamación ! al principio de la pareja de corchetes que definen el nombre del enlace. 

```
![Con titulo](img/payaso.jpg "payaso")
```

![payaso con titulo](img/payaso.jpg "payaso")

# tablas
Se puede especificar la alineación de cada columna mediante la adición de dos puntos a las líneas de separación.  
Dos puntos a la izquierda de la línea de separación hará que la columna esté alineada a la izquierda, dos puntos a la derecha de la línea hará que la columna esté alineada a la derecha, dos puntos en ambos lados significa que la columna se alinea al centro.

```
| Elemento | Cantidad | Precio |
| :------- | :------: | -----: |
| Item 1   | 15       | 150€   |
| Item 2   | 3250     | 23,65€ |
```

| Elemento | Cantidad | Precio |
| :------- | :------: | -----: |
| Item 1   | 15       | 150€   |
| Item 2   | 3250     | 23,65€ |

# otras chuletas 
[chuleta de Markdown en castellano joedicastro](http://joedicastro.com/pages/markdown.html)

# enlaces de interes
* [wikipedia](https://es.wikipedia.org/wiki/Markdown)
* [oficial documentación](http://daringfireball.net/projects/markdown/syntax)
* [generador de tablas](http://www.tablesgenerator.com/markdown_tables#)





[Enlace a esa cabecera](#cabecera1)