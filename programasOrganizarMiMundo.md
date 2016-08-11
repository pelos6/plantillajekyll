---
layout: default
---
[inicio](inicio.html) / [miMundo](miMundo.html) / programasOrganizarMiMundo
# programas para organizar mi mundo
<!-- MarkdownTOC -->

- [Enlaces para generar una página web estatica en gitHub](#enlaces-para-generar-una-página-web-estatica-en-github)
- [escribirlo en Markdown](#escribirlo-en-markdown)
- [repositorio](#repositorio)
- [buscar una forma de publicar facilmente esta información](#buscar-una-forma-de-publicar-facilmente-esta-información)
- [usar todo para la lista de tareas.](#usar-todo-para-la-lista-de-tareas)

<!-- /MarkdownTOC -->
# Enlaces para generar una página web estatica en gitHub
- [metodo para publicar en gitHub](https://24ways.org/2013/get-started-with-github-pages/)
- [razones para usar este método](razonesUsarGithubPagina.html)

# escribirlo en [Markdown](markdown.html) 
- usando [SublimeText](sublimeText.html) como editor
- uso sublimeText 3 de 32 bits portable que esta en este directorio
     + C:\nube\MEGA\portables\sublimeText3_32_mundo para poderlo usar en el curro 
     + dejo ese sublime portable para esta documentación y en el resto de instalaciones si que instalo más plugins.
     + uso una [plantilla](plantilla.html) al generar el html se usa esa plantilla y el contenido se inserte en HEAD y en BODY 
        - Esta plantilla debe estar en el directorio donde este el ejecutable de sublimeText.exe
        - El uso de esta plantilla se debe definir en los settingd de MarkdownPreview 
        ````
            "html_template": "plantilla.html",
            "file_path_conversions": "relative",
            "skip_default_stylesheet": true
        ````
- pongo migas de pan donde es relevante 
     + inicio / mi mundo / cursos / front-End JavaScript Frameworks AngularJS
- Al instalar por ejemplo SublimeGit se renderiza mal el html con MarkdownPreview. Reinicio Sublime (mundo) y vuelve a funcionar bien!!.
- aunque al cambiar ya no 
    - uso Brackets con el plugin Markdown Preview porque es más facil ver lo que estas escribiendo
    - instalo MarkdownPad 2 para probar en 
         C:\Program Files (x86)\MarkdownPad 2
        pero lo desinstalo por que te pide actualizar a pro y da problemas al hacer el previo
#  repositorio
- 06/08/2016 uso [GitHub](https://github.com/pelos6/mundo)
- antes [bitBucket](bitBucket.html)

# buscar una forma de publicar facilmente esta información
- En bitbucket siguiendo este [tutorial](https://confluence.atlassian.com/bitbucket/publishing-a-website-on-bitbucket-cloud-221449776.html)
- Pero el nombre de la web debe llevar el nombre del usuario tipo http://pelos6.bitbucket.org/ lo que limita la utilidad 
    - esto es medio verdad pues hay dos formas de hacerlo una para paginas de tipo personal que es esta y otra para páginas de proyectos
- la ventaja de BitBucket sobre git con los repositorios privados no sirve aqui pues esta url es accesible para todo el mundo aunque venga de un repositorio privado.
    - En gitHub siguiendo este otro [tutorial](http://blog.teamtreehouse.com/using-github-pages-to-host-your-website) o [este del propio GitHub](https://pages.github.com/)
- clonar en gh-pages parece obligatorio para que funcione aunque no entiendo mucho porque.
- sale este error al cargar los cdn. Lo soluciono cambiandolos a https y para eso tengo que cambiarlos en la [plantilla](plantilla.html)
```
    This request has been blocked; the content must be served over HTTPS. 
```
- secuencia de publicación
     + guardo los cambios en md y genero el html control + b
     + git add .
     + git commit -m "comentario"
     + git push -u origin gh-pages
# usar [todo](C:\nube\MEGA\portables\plainText\todo.txt) para la lista de tareas.
