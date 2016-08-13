---
layout: default
title: jekyll
---
[inicio](index.html) / [programacion](programacion.html) /  {{ page.title }}
<!-- MarkdownTOC -->

- [Proposito](#proposito)
- [instalación](#instalación)
- [instalar chocolatey](#instalar-chocolatey)
- [instalar ruby](#instalar-ruby)
- [instalar Jekyll](#instalar-jekyll)
- [usar jekyll](#usar-jekyll)
- [inicio rápido](#inicio-rápido)
- [prueba rápida](#prueba-rápida)
- [otro inteno con jekyl nueva](#otro-inteno-con-jekyl-nueva)

<!-- /MarkdownTOC -->

# Proposito
- Ver como se usa [jekyll](http://jekyllrb.com/) y que utilidades puedo usar
- Empiezo con este [post](https://24ways.org/2013/get-started-with-github-pages/)  

# instalación
- Sigo este [enlace](https://davidburela.wordpress.com/2015/11/28/easily-install-jekyll-on-windows-with-3-command-prompt-entries-and-chocolatey/)

# instalar chocolatey  
- desde una consola con privilegios de administrador
- para instalar Chocolatey  
```
@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
```

```
    Ensuring chocolatey commands are on the path
    Ensuing chocolatey.nupkg is in the lib folder
```
- para que chocolatey funcione es necesario reabrir la consola 
- para ver que versión se ha instalado se teclea simplemente 
 
```
    choco
    Chocolatey v0.9.10.3
```  

# instalar ruby
````
choco install ruby -y
ruby has been installed.
Adding 'C:\tools\ruby23\bin' to the local path
````
````
ruby -v
ruby 2.3.0p0 (2015-12-25 revision 53290) [x64-mingw32]
````

# instalar Jekyll
````
gem install jekyll
jekyll -v
jekyll 3.2.1
````

# usar jekyll
```
jekyll new pruebas
cd pruebas
jekyll serve --watch  
``` 
- pero da este error  

        C:/tools/ruby23/lib/ruby/2.3.0/rubygems/core_ext/kernel_require.rb:55:in
        `require': cannot load such file -- bundler (LoadError)
        from C:/tools/ruby23/lib/ruby/2.3.0/rubygems/core_ext/kernel_require.rb:55:in `require'
        from C:/tools/ruby23/lib/ruby/gems/2.3.0/gems/jekyll-3.2.1/lib/jekyll/plugin_manager.rb:34:in `require_from_bundler'
        from C:/tools/ruby23/lib/ruby/gems/2.3.0/gems/jekyll-3.2.1/exe/jekyll:9:in `<top (required)>'
        from C:/tools/ruby23/bin/jekyll:23:in `load'
        from C:/tools/ruby23/bin/jekyll:23:in `<main>'

- intento instalar bundler

        gem install bundler
        bundle install
- Ahora si que funciona el servidor  
```
http://127.0.0.1:4000/ 
```
- y veo la web generada

# inicio rápido
1. hacer un fork del repositorio https://github.com/javieriranzo3/plantillajekyll  
2. luego lo clono en el directorio que quieras y ya se puede modificar

# prueba rápida
1. creo el repositorio vacio pruebajekyll  
2. lo clono en 
C:\nube\MEGA\programacion\HtmlCssEstatico\jekyll\  

        git clone https://github.com/pelos6/pruebajekyll.git
        cd pruebajekyll
        git checkout --orphan gh-pages

3. luego desde   
C:\nube\MEGA\programacion\HtmlCssEstatico\jekyll\  


        jekyll new pruebajekyll  
        cd pruebajekyll     
        jekyll serve --watch  

4. cambio en  `_config.yml`  

        name: javier iranzo
        markdown: redcarpet
        pygments: true
        baseurl: /christmas-recipes

5. el problema viene porque jekyll usa unos includes que gitHub pages aún no sieve por eso incluso la plantilla mínima da problemas  
6. con redcarpet y con pygments que no son esenciales para lo que quiero así que lo quito

        http://127.0.0.1:4000/pruebajekyll/

6. y veo la web

7. lo subo a git pero da un error que manda un correo a mi cuenta.
    - sobre about.md. sobre unos include que no puede resolver
    - luego otro en main.css con un include que comento con un `import minima`

        https://pelos6.github.io/pruebajekyll/
    - ya lo veo pero sin los css 
    - los archivos md tienen que tener un encabezado especial al inicio para que se conviertan a html  

            ---  
            title: Inicio  
            permalink: /inicio/  
            ---

    - nada mas ponerlo con el serve en marcha se genera un directorio inicio donde esta el archivo convertido a html

# otro inteno con jekyl nueva
- lo que pasa es que no resuelve minima
- sigo este post 
http://stackoverflow.com/questions/38772179/jekyll-work-in-local-but-not-work-github-file-to-import-not-found-or-unreadable  
c:\nube\MEGA\programacion\HtmlCssEstatico\jekyll\nueva>bundle show minima  
C:/tools/ruby23/lib/ruby/gems/2.3.0/gems/minima-1.0.1

- se genera bien pero falta main.css pues el que esta es main.scss
- lo copio del directorio _site pues en local funciona.
- pero no recupera el css nuevo
- puede ser un problema de directorios 
- modifico en `_config.yml`

        baseurl: "/nueva"

- era eso
pruebo a editar about.md desde el editor de git hub y en un minuto lo veo reflejado
- nota esto obligará a hacer un git pull para sincronicar esos cambios

- los archivos *.md que pongo en el directorio 
C:\nube\MEGA\programacion\HtmlCssEstatico\jekyll\nueva
- luego los abro y añado  

        ---
        layout: default
        title: programación
        ---

- jekyll genera el correspondiente html con la plantilla default y pone en el menu la opción programación

