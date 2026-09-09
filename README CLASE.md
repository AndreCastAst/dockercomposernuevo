README copiado de **Ejercicio Docker Compose** en Canvas. Se cambiaron los nombres de las apis, el POSTGRES_PASSWORD y se respondió a los tipos de redes y volúmenes.

# Laboratorio 02

Hoy utlizaremos docker compose para poder desplegar un servicio web y una base de datos

STACK Tecnico

API

- Aplicación JAVA dockerizarla (crear la imagen)
  - docker pull nmatsui/hello-world-api
- intelligent_tharp 3001
- practical_shannon 3000
- $ docker run -d --rm -p 3000:3000 nmatsui/hello-world-api
- 

BD PostgreSQL
docker run --name some-postgres -e POSTGRES_PASSWORD=Contrasena123 -d postgres

COMANDOS

Deben especificar los comandos que voy a ejecutar

```bash
docker compose up -d
```

CONFIGURACIONES
.env

```
VAR=VALUE
```

# Actividad

Trabajar un docker compose, especificando configuración y comandos para despliegue. Debe permitir lo siguiente:

- 3 copias de una API build local |
- Configuración BD |
- Uso de volúmenes |
- Uso de variables de entorno |
- En README. Responder los tipos de redes y los tipos de volumen que existen en docker |

Redes:

- Bridge: Defaullt, pero sirve para dentro de un mismo equipo.
- Host: Conecta al contenedor con nuestra máquina, entre IPs y puertos.
- None: No es que sea una red, es elegir no tener una. Aisla al contenedor del host y de internet.
- Overlay: Usado para entre varios hosts(nodos). Relacionado a Docker Swarm
- Macvlan: Hace a un contenedor reconocible por la red local, tal cual como tu pc.

Volúmenes:

- Named Volume: Asignación de nombre manual. Se almacenan en el host pero se controla por el docker. Recomendada para producción.
- Anonymus Volume: Asignación de nombre automática. ID ilegible. Dependientes del contenedor asociado.
- Bind Mounts: Asocia cualquier archivo del host al contenedor.
- Tmpfs Mounts: Usa la RAM del host como almacén de datos, es decir, se vuelven datos temporales.



- Hacer uso de Conventional Commits |
- Repositorio publico |
- Uso de .gitignore |
- Opcional: Capturas de su proyecto desplegado |
