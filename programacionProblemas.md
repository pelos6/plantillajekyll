---
layout: default
title: programación problemas
---
[inicio](index.html)  / [programacion](programacion.html) / programacion problemas 
#  Programación Problemas
<!-- MarkdownTOC -->

- [Proposito](#proposito)
- [Bower](#bower)
- [Sublime 3](#sublime-3)

<!-- /MarkdownTOC -->

# Proposito
- Los problemas que voy encontrando y (a veces) resolviendo.
#  Bower
bower install me da este error
```
bower install
"appbower" no se reconoce como un comando interno o externo,
programa o archivo por lotes ejecutable.
```
asi que instalo bower otra vez
```
npm install -g bower
```
da ahora este error
```
bower invalid-meta  The "name" is recommended to be lowercase, can contain digits, dots, dashes
```
reviso bower.json y name es correcto !!!!
```
bower install --verbose -- force
```  
ahora funciona 

# Sublime 3
Error loading syntax file
"Package/Markdown/Markdown.tmLanguage": Unable to open Package/Markdown/Markdown.tmLanguage 
Esto pasaba si había un archivo md abierto por defecto lo que provocaba e intento de cargar la sintaxis para este tipo de archivo que estaba sustituida por el plugin markdownEditing
https://github.com/SublimeText-Markdown/MarkdownEditing/issues/205

