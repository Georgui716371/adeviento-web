# Calendario de aDEViento Web

[![Python](https://img.shields.io/badge/Python-3.11+-yellow?style=for-the-badge&logo=python&logoColor=white&labelColor=101010)](https://python.org)
[![Reflex](https://img.shields.io/badge/Reflex-0.3.4+-5646ED?style=for-the-badge&logo=python&logoColor=white&labelColor=101010)](https://reflex.dev)
[![NES.css](https://img.shields.io/badge/NES.css-2.3.0-007bff?style=for-the-badge&logo=css3&logoColor=white&labelColor=101010)](https://nostalgic-css.github.io/NES.css)
[![Vercel](https://img.shields.io/badge/Vercel-static-gray?style=for-the-badge&logo=vercel&logoColor=white&labelColor=101010)](https://vercel.com)

## Proyecto web "Calendario de aDEViento" con Python puro y Reflex

![https://adviento.dev](./images/preview.gif)

> El "Calendario de aDEViento" es una actividad en la que cada día (durante el adviento) se sortea un regalo relacionado con programación y desarrollo de software (libros, cursos…). Su finalidad es ayudar a compartir conocimiento y fomentar el aprendizaje en comunidad.

### Visita [https://adviento.dev](https://adviento.dev)

#### Desarrollo realizado en directo desde [Twitch](https://twitch.tv/mouredev)
> ##### Si consideras útil el proyecto, apóyalo haciendo "★ Star" en el repositorio. ¡Gracias!

## Tutorial

*[Próximamente]* Publicaré un vídeo con todo el proceso de desarrollo y despliegue de la web.

Sígueme en mi canal de YouTube secundario "[MoureDev TV](https://youtube.com/@mouredevtv)" para no perdértelo.

## Proyecto

Esta es la estructura general del proyecto.

* **adeviento_web**: código fuente principal
	* **adeviento_web.py**: index del sitio web
	* **constants.py**: constantes utilizadas en el sitio
	* **styles**: directorio de estilos (css, colores y fuentes)
	* **views**: directorio de vistas (secciones gráficas)
	* **components**: directorio de componentes (elementos gráficos con menor entidad que una vista)
* **assets**: recursos gráficos y utilidades JavaScript (nive y cuenta atrás)
* **rxconfig.py**: configuración principal del proyecto (por defecto)
* **requirements.txt**: dependencias del proyecto para su ejecución
* **assets**: recursos gráficos y utilidades JavaScript (nive y cuenta atrás)
* **build.sh**: script de generación estática de la web para producción
* **[generado] public**: empaquetado estático del proyecto que se despliega en producción (HTML, CSS, JS e imágenes)

## Configuración en local

1. Haz un `Fork` del repositorio.

2. Clona ese repositorio en tu máquina local.

    ```bash 
    git clone https://github.com/<USERNAME>/adeviento-web.git
    ```

3. Navega al directorio del proyecto.

    ```bash
    cd adeviento
    ```

4. Crea un entorno virtual.

    ```bash
    python3 -m venv venv
    ```

5. Actuva el entorno virtual.

    ```bash
    source venv/bin/activate
    ```

6. Instala las dependencias.

    ```bash
    python -m pip install -r requirements.txt
    ```

7. Inicializa el proyecto de Reflex.

    ```bash
    reflex init
    ```

8. Ejecuta el proyecto en local.

    ```bash
    reflex run
    ```

    *Podrás acceder a él entrando en la url `http://localhost:3000/` desde el navegador.*
    
> Tienes más la información sobre [Reflex](https://reflex.dev/) en su [documentación oficial](https://reflex.dev/docs).

## Despliegue

Para realizar el despliegue del proyecto se ha creado un archivo `build.sh` que se encarga de ejecutar el flujo necesario para generar el directorio `public` con todos los recursos estáticos que necesita el servidor web. 

Todo el proceso de empaquetado para producción podría ser delegado en el servidor, pero el repositorio cuenta siempre con el directorio `public` para que así puedas revisar el contenido estático de la web sin necesidad de ejecutar el script `build.sh`.

```bash
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
reflex init
reflex export --frontend-only
rm -fr public
unzip frontend.zip -d public
rm -f frontend.zip
deactivate
```

*Básicamente, prepera el entorno, instala dependencias, inicializa el proyecto, crea la construcción de producción, y la descomprime.*

> El proyecto se puede desplegar en cualquier proveedor o servidor que soporte recursos estáticos.
> 
> [adviento.dev](https://adviento.dev) se encuentra desplegado en [Vercel](https://vercel.com).

Configuración en Vercel:

* Se ha asociado el repositorio de GitHub al proyecto (para que cada `push` en la rama `main` desencadene un nuevo despliegue)
* Build & Development Settings: Other
* Root Directory: `public` (que contiene el empaquetado estático para producción)
* Custom Domain: adviento.dev 

## Recursos utilizados

![Python](https://img.shields.io/github/stars/python/cpython?label=Python&style=social)
![Reflex](https://img.shields.io/github/stars/reflex-dev/reflex?label=Reflex&style=social)
![NES.css](https://img.shields.io/github/stars/nostalgic-css/NES.css?label=NES.css&style=social)
![Vercel](https://img.shields.io/github/stars/vercel/vercel?label=Vercel&style=social)

* Lenguaje: [Python](https://www.python.org/)
* Framework: [Reflex](https://reflex.dev/)
* CSS: [NES.css](https://nostalgic-css.github.io/NES.css/)
* Fuente: [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P)
* Hosting: [Vercel](https://vercel.com/)

## Curso de Python y Reflex

<a href="https://github.com/mouredev/python-web"><img src="https://raw.githubusercontent.com/mouredev/python-web/main/Images/header.jpg"/></a>

Curso gratis para aprender desarrollo frontend Web con Python puro desde cero con Reflex. Las tecnologías usadas para desarrollar el proyecto del "Calendario de aDEViento". También tengo un curso de Python desde cero para principiantes.

[![Curso Python Web](https://img.shields.io/github/stars/mouredev/python-web?label=Curso%20Python%20web&style=social)](https://github.com/mouredev/python-web)
[![Curso Python](https://img.shields.io/github/stars/mouredev/hello-python?label=Curso%20Python&style=social)](https://github.com/mouredev/python-web)

#### Puedes apoyar mi trabajo haciendo "☆ Star" en el repo o nominarme a "GitHub Star". ¡Gracias!

[![GitHub Star](https://img.shields.io/badge/GitHub-Nominar_a_star-yellow?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://stars.github.com/nominate/)

Si quieres unirte a nuestra comunidad de desarrollo, aprender programación de Apps, mejorar tus habilidades y ayudar a la continuidad del proyecto, puedes encontrarnos en:

[![Twitch](https://img.shields.io/badge/Twitch-Programación_en_directo-9146FF?style=for-the-badge&logo=twitch&logoColor=white&labelColor=101010)](https://twitch.tv/mouredev)
[![Discord](https://img.shields.io/badge/Discord-Servidor_de_la_comunidad-5865F2?style=for-the-badge&logo=discord&logoColor=white&labelColor=101010)](https://mouredev.com/discord)
[![Link](https://img.shields.io/badge/Links_de_interés-moure.dev-39E09B?style=for-the-badge&logo=Linktree&logoColor=white&labelColor=101010)](https://moure.dev)

## ![https://mouredev.com](https://raw.githubusercontent.com/mouredev/mouredev/master/mouredev_emote.png) Hola, mi nombre es Brais Moure.
### Freelance full-stack iOS & Android engineer

[![YouTube Channel Subscribers](https://img.shields.io/youtube/channel/subscribers/UCxPD7bsocoAMq8Dj18kmGyQ?style=social)](https://youtube.com/mouredevapps?sub_confirmation=1)
[![Twitch Status](https://img.shields.io/twitch/status/mouredev?style=social)](https://twitch.com/mouredev)
[![Discord](https://img.shields.io/discord/729672926432985098?style=social&label=Discord&logo=discord)](https://mouredev.com/discord)
[![Twitter Follow](https://img.shields.io/twitter/follow/mouredev?style=social)](https://twitter.com/mouredev)
![GitHub Followers](https://img.shields.io/github/followers/mouredev?style=social)
![GitHub Followers](https://img.shields.io/github/stars/mouredev?style=social)

Soy ingeniero de software desde hace más de 13 años. Desde hace 5 años combino mi trabajo desarrollando Apps con creación de contenido formativo sobre programación y tecnología en diferentes redes sociales como **[@mouredev](https://moure.dev)**.

### En mi perfil de GitHub tienes más información

[![Web](https://img.shields.io/badge/GitHub-MoureDev-14a1f0?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://github.com/mouredev)
