---
layout: default
title: Instalacion y creacion de un tema con jekyll
permalink: /temas-jekyll/
---

# Instalacion y creacion de un tema con jekyll

![alt text](https://themefisher.com/blog-thumb/best-jekyll-themes.webp)
## Introducción a jekyll themes

Jekyll es un generador de sitios estáticos que permite crear blogs y páginas web de forma sencilla. Uno de sus aspectos más destacados son los **temas**, que ofrecen estilos y funcionalidades predefinidos, facilitando el diseño y la personalización del sitio sin necesidad de escribir código desde cero. Los temas en Jekyll suelen incluir:

1. **Diseño Responsivo**: Muchos temas están diseñados para adaptarse a diferentes dispositivos, garantizando una buena experiencia de usuario en móviles y tabletas.

2. **Personalización**: A través de archivos de configuración y estilos CSS, los usuarios pueden personalizar colores, fuentes y otros elementos visuales para alinearse con su marca o estilo personal.

3. **Funcionalidades Integradas**: Los temas a menudo incluyen características como menús de navegación, galerías de imágenes, y secciones para publicaciones, facilitando la organización del contenido.

4. **Soporte para Plugins**: Algunos temas permiten la integración de plugins para añadir funcionalidades adicionales, como optimización SEO o sistemas de comentarios.

## Buscamos el tema

Por defecto con jekyll las paginas se crean con un tema llamado ~~minima~~ , como el mismo nombre dice este tema te da lo minimo para poder utilizar jekyll por eso vamos a buscar nuevos temas , esos temas lo podemos encontrar en los siguientes enlaces;

| Plataforma                         | Enlace                                             |
|-----------------------------------|---------------------------------------------------|
| Jekyll Themes                     | [jekyllthemes.org](http://jekyllthemes.org/)     |
| RubyGems (Jekyll Themes Search)  | [rubygems.org](https://rubygems.org/search?query=jekyll-theme-) |
| Jamstack Themes                   | [jamstackthemes.dev](https://jamstackthemes.dev/ssg/jekyll/) |
| GitHub (Jekyll Themes)            | [github.com](https://github.com/topics/jekyll-theme) |
| Jekyll Themes IO                  | [jekyllthemes.io](https://jekyllthemes.io/)      |
| Jekyll Themes                     | [jekyll-themes.com](https://jekyll-themes.com/)  |

## Instalacción

Primero lo que debemos de hacer es añadir al GEMFILE el enlace que nos muestre en la inslacion del tema.
`echo "gem 'jekyll-theme-modernist', '~> 0.2.0'" >> Gemfile`
En este caso se esta utilizando el tema **modernist** pero se aplica con cualquiera.
Luego utilizaremos el comando `bundle install` para instalar las gemas del tema.
Segido lo que haremos es modificar el fichero _config.yml y en la parte de ;
```
# Build settings
theme: minima
plugins:
  - jekyll-feed
```
Cambiaremos minima por el nombre de nuestro tema;
```
# Build settings
theme: jekyll-theme-modernist
plugins:
  - jekyll-feed
```
Ahora lo que haremos es un `bundle update` para al igual que bundle install, bundle update resuelve las dependencias para asegurarse de que las nuevas versiones de las gemas sean compatibles entre sí.

y ya tendriamos nuestro tema añadido correctamente.
