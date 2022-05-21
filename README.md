<div align="center">
<table>
    <theader>
        <tr>
            <th><img src="https://github.com/rescobedoulasalle/git_github/blob/main/ulasalle.png?raw=true" alt="EPIS" style="width:50%; height:auto"/></th>
            <th>
                <span style="font-weight:bold;">UNIVERSIDAD LA SALLE</span><br />
                <span style="font-weight:bold;">FACULTAD DE INGENIERÍAS</span><br />
                <span style="font-weight:bold;">DEPARTAMENTO DE INGENIERÍA Y MATEMÁTICAS</span><br />
                <span style="font-weight:bold;">CARRERA PROFESIONAL DE INGENIERÍA DE SOFTWARE</span>
            </th>            
        </tr>
    </theader>
    
</table>
</div>

<div align="center">
<span style="font-weight:bold;">GUÍA DE LABORATORIO</span><br />
</div>

<table>
    <theader>
        <tr><th colspan="2">INFORMACIÓN BÁSICA</th></tr>
    </theader>
<tbody>

<tr><td>TÍTULO DE LA PRÁCTICA:</td><td>Docker</td></tr>
<tr><td colspan="2">RECURSOS:
    <ul>
        <li><a href="https://www.docker.com/">Sitio oficial del Proyecto Docker</a></li>
        <li><a href="https://github.com/moby/moby">El Proyecto Moby</a></li>
        <li><a href="http://www.haifux.org/lectures/320/netLec8_final.pdf">Contenedores de Linux y la nube del futuro</a></li>
        <li><a href="https://dondocker.com/orquestando-contenedores-docker-para-tener-un-joomla-y-un-mysql-en-diferentes-hosts/">Joomla y MySQL con Docker</a></li>
        <li><a href="https://www.youtube.com/watch?v=VeiUjkiqo9E#t=60">Tutorial de docker en Youtube</a></li>
        <li><a href="https://web.archive.org/web/20130808043357/http://www.linux.com/news/enterprise/cloud-computing/731454-docker-a-shipping-container-for-linux-code/">Docker: un 'Desplegador de contenedores' para el código de Linux</a></li>
        <li><a href="https://www.ionos.es/digitalguide/servidores/configuracion/tutorial-docker-instalacion-y-primeros-pasos/">Tutorial de Docker: instalar y gestionar la plataforma de contenedores</a></li>
        <li><a href="https://hub.docker.com/">Docker Hub</a></li>
        <li><a href="https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-es">Cómo instalar y usar Docker en Ubuntu 20.04</a></li>
    </ul>
</td>
</<tr>
<tr><td colspan="2">ESTUDIANTE:
    <ul>
        <li>Valeria Alejandra Goyzueta Torres  - vgoyzuetat@ulasalle.edu.pe</li>
    </ul>
</td>
</<tr>
</tdbody>
</table>

# Docker

[![License][license]][license-file]
[![Downloads][downloads]][releases]
[![Last Commit][last-commit]][releases]

[![Debian][Debian]][debian-site]
[![Git][Git]][git-site]
[![GitHub][GitHub]][github-site]
[![Vim][Vim]][vim-site]
[![Java][Java]][java-site]

#

## OBJETIVOS Y TEMAS

### OBJETIVOS
- Aprender a desplegar contenedores con Docker.

### TEMAS
- Docker.
- Docker vs VMs
- Arquitectura de Docker
- Comandos en Docker

## EJERCICIOS PROPUESTOS

-   1. Realice los cambios necesarios para que la imagen que ud creo a partir de un contenedor personalizado se pueda acceder al servidor web desde el equipo anfitríon.
    ```sh
    docker run -p 8088:80 rcd22image
    ```
-   2. Crear dos contenedores que puedan comunicarse: ping.
    <br>
    Para la creación de dos contenedores, que son los encargados de hacerse ping se tiene que tener una red en común entre ambon contenedores, para que estos ya puedan comunicarse. Primero, hay que tener en consideración que ya hayamos hecho un pull a alguna imagen y hayamos creado unos contenedores que surgen en base a esa imagen a la que le hemos hecho pull. Para ello usamos el comando *docker pull debian*, y en base a ello, crearemos dos contenedores, haciendo uso del comando *docker create --name nombre imagen*. 
    ![Create](CreateDocker.jpg)
    <br>
    Una vez realizado eso, se crea una red a las que vamos a conectar nuestros contenedores *docker create network nombredelared*. y corremos los contenedores: *docker run --network red --name nombre nombreimagen*.
    ![Run](runDocker.jpg)
    Instalaremos los paquetes necesarios para poder hacer ping y haremos ping, entre ambos contenedores con el comando *ping direccionip*, corroborando de esta manera que pertenecen a la misma red.
    ![Install](installDocker.jpg)
    ![Ping](pingDocker.jpg)
    <br>
-   3. Investigar acerca de la ejecución de programas con interfaz gráfica dentro de contenedores Docker.

#

## CUESTIONARIO

- ¿Qué son los "cgroups" del kernel de Linux? y ¿Qué diferencia más interesante encontró entre las versiones 1 y 2?
   Los cgroups, que en su forma no abreviada se conocen como: "control groups" es una característica del kernel de Linux que permite limitar, llevar cuenta y aislar    los recursos de uso: CPU, memoria, etc. De un grupo de procesos. Permite organizar los procesos de una manera jerárquica los cuales son limitados y monitoreados. Esta jerarquía se define creando, eliminando y renombrando subdirectorios dentro del sistema de archivos cgroup. Existen diversas difencias entre ambas versiones sacadas a la luz computacional, entre ellas tenemos: La versión 1 

- ¿Qué son los "namespaces" del kernel de Linux? y ¿Cuáles son los tipos de "namespaces"?
- ¿Qué diferencia puede resaltar entre LXC y libcontainer?
- Investigue acerca del malware Doki y explique brevemente.
- ¿Hasta que punto la empresa RedHat se ha comprometido con el proyecto Docker?

#

## REFERENCIAS
-   [Sitio oficial del Proyecto Docker][Docker-site]
-   [Proyecto Moby][Moby-Github]
-   [Diapositivas "Contenedores de Linux y la nube del futuro" por Rami Rosen][Containers-PDF]
-   [Docker para un proyecto Joomla-MySQL][Joomla-MySQL]
-   [Tutorial de Docker en Youtube][Docker-Tutorial-Youtube]
-   [Cómo instalar y usar Docker en Ubuntu 20.04][Cómo instalar y usar Docker en Ubuntu 20.04]

#

[license]: https://img.shields.io/github/license/rescobedoulasalle/git_github?label=rescobedoulasalle
[license-file]: https://github.com/rescobedoulasalle/git_github/blob/main/LICENSE

[downloads]: https://img.shields.io/github/downloads/rescobedoulasalle/git_github/total?label=Downloads
[releases]: https://github.com/rescobedoulasalle/git_github/releases/

[last-commit]: https://img.shields.io/github/last-commit/rescobedoulasalle/git_github?label=Last%20Commit

[Debian]: https://img.shields.io/badge/Debian-D70A53?style=for-the-badge&logo=debian&logoColor=white
[debian-site]: https://www.debian.org/index.es.html

[Git]: https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white
[git-site]: https://git-scm.com/

[GitHub]: https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white
[github-site]: https://github.com/

[Vim]: https://img.shields.io/badge/VIM-%2311AB00.svg?style=for-the-badge&logo=vim&logoColor=white
[vim-site]: https://www.vim.org/

[Java]: https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white
[java-site]: https://docs.oracle.com/javase/tutorial/

[Docker-site]: https://www.docker.com/
[Moby-Github]: https://github.com/moby/moby
[Containers-PDF]: http://www.haifux.org/lectures/320/netLec8_final.pdf
[Joomla-MySQL]: https://dondocker.com/orquestando-contenedores-docker-para-tener-un-joomla-y-un-mysql-en-diferentes-hosts/
[Docker-Tutorial-Youtube]: https://www.youtube.com/watch?v=VeiUjkiqo9E#t=60

[Docker: A 'Shipping Container' for Linux Code]: https://web.archive.org/web/20130808043357/http://www.linux.com/news/enterprise/cloud-computing/731454-docker-a-shipping-container-for-linux-code/
[Tutorial de Docker: instalar y gestionar la plataforma de contenedores]: https://www.ionos.es/digitalguide/servidores/configuracion/tutorial-docker-instalacion-y-primeros-pasos/

[Docker-Hub]: https://hub.docker.com/

[Cómo instalar y usar Docker en Ubuntu 20.04]:https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-es


[![Debian][Debian]][debian-site]
[![Git][Git]][git-site]
[![GitHub][GitHub]][github-site]
[![Vim][Vim]][vim-site]
[![Java][Java]][java-site]

[![License][license]][license-file]
[![Downloads][downloads]][releases]
[![Last Commit][last-commit]][releases]

