---
layout: default
title: plantilla simple
---
[inicio](index.html) / [plantillas](plantillas.html) / plantilla simple

<!-- MarkdownTOC -->

- [Proposito](#proposito)
- [titulo](#titulo)

<!-- /MarkdownTOC -->

# Proposito
- tener la plantilla de todos los documentos para que sean coherentes
- poner en este documento todas las cosas que se pueden usar

#  titulo
- viene en la plantilla default
- viene en la miga de pan

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


