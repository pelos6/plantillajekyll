---
layout: default
---
# MarkdownPreview

Se puede usar una plantilla para generar el html
en el archivo 
C:\nube\MEGA\portables\sublime\sublime\Data\Packages\Markdown Preview\MarkdownPreview.sublime-settings

     "html_template": "plantilla.html",
     "skip_default_stylesheet": true,
 plantilla.html colocada en el directorio de trabajo del programa 
 C:\nube\MEGA\portables\sublime\sublime
 es un principio una copia de customized-template-sample.html
 el resto de las notas no son necesarias ... pero por si acaso 
con la propiedad parser del plugin markdown preview 
C:\nube\MEGA\portables\sublime\sublime\Data\Packages\Markdown Preview\MarkdownPreview.sublime-settings
```
    "parser": "github",
```
para que genere el html mas ancho estilo github.
pero como me da problemas con MarkdownTOC y simplemente quiero que sea mas ancho el body cambio en 
C:\nube\MEGA\portables\sublime\sublime\Data\Packages\Markdown Preview\markdown.css
```
body {
 /* javier
 width: 45em;
 modificado para hacerlo más ancho */
  width: 980px; 
```

# problemas
deja de tomar la plantilla.
al hacer el build en la consola sale siempre 0 segundos.
reinicio sublime y se soluciona
instalaba git ....
