---
layout: default
title: git chuleta
---
[inicio](index.html)  / [programacion](programacion.html) / [git](git.html) / {{ page.title }}
<!-- MarkdownTOC -->

- [secuencia habitual](#secuencia-habitual)
- [deshacer unos cambios](#deshacer-unos-cambios)
- [repositorios remotos](#repositorios-remotos)
- [configuración](#configuración)
- [problemas con varios usuarios](#problemas-con-varios-usuarios)
- [actualizar la copia local con el repositorio remoto](#actualizar-la-copia-local-con-el-repositorio-remoto)
- [git y subliem text 3](#git-y-subliem-text-3)
- [enlaces útiles](#enlaces-útiles)

<!-- /MarkdownTOC -->

# secuencia habitual  
```
git add -A
git commit -m "mensaje del commit"
git push -u origin master
```

* git add -A 
en git 1.x almacena todos los archivos ya sean nuevos, modificados o borrados
en git 2.x tambien
- git add . 
en git 1.x almacena todos los archivos ya sean nuevos o modificados no los borrados
en git 2.x almacena también los borrados
- git push -u 
    + origin es la rama local
    + master suele ser la rama en el repositorio remoto pero puede ser gh-pages para esta documentación

# deshacer unos cambios
```
git reset --hard 
Please, commit your changes or stash them before you can merge.
```

# repositorios remotos
para ver la url 

```
git remote -v 
```

# configuración
- muestra la lista de los parametros de configuración  
```
git config --list  
```  

# problemas con varios usuarios  

```
git remote rm origin

git remote add origin https://javieriranzo3@github.com/javieriranzo3/plantillajekyll.git
git config remote.origin.url https://javieriranzo3:pelos678@github.com/javieriranzo3/plantillajekyll.git
```

esto soluciona el problema que decia 

```
c:\nube\MEGA\programacion\HtmlCssEstatico\jekyll\plantillajekyll>git push -u origin gh-pages
remote: Permission to javieriranzo3/plantillajekyll.git denied to pelos6.
fatal: unable to access 'https://javieriranzo3@github.com/javieriranzo3/plantillajekyll.git/':   
The requested URL returned error: 403
```

# actualizar la copia local con el repositorio remoto  
```
git pull

C:\nube\MEGA\mundo>git pull
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/pelos6/mundo
   a56588c..0d8d6f3  gh-pages   -> origin/gh-pages
Updating a56588c..0d8d6f3
Fast-forward
 miMundo.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-) 
```


# git y subliem text 3
parece que al instalar el package en sublime algo se desconfigura con 
el paquete de markdownpreview 
no coje la plantilla. 
tengo que quitar el package git y volver a abrir sublime ..!!!! 

# enlaces útiles
[Comandos básicos en castellano](http://rogerdudler.github.io/git-guide/index.es.html)
