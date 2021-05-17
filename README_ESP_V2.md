💻
# Traducción al Español
# Descripción

Kubify es una herramienta CLI para administrar el ciclo de vida de desarrollo e implementación de microservicios.

Kubify es DevEx (Developer-First) Kubernetes Turn Key Full SDLC Framework (DevOps Solution) que le permite realizar pruebas rápidas de toda la infraestructura localmente (de la misma manera que se implementa), lo que genera una calidad asombrosa en las confirmaciones de código de los servicios. 

Haga que Kubernetes sea fácil de usar adoptando 1 Yaml por servicio, 1 Yaml por Env, 1 Carpeta para FE y 1 Carpeta para BE, la estrategia de automatización clara DevEx completa de Kubify y haga felices a nuestros ingenieros Devs / DevOps / DevSecOps. 

Piense en la eficiencia y la felicidad del equipo de desarrollo. 

Piense en la incorporación reducida de semanas a solo 5 minutos. Eso debería decir mucho.


Este es un software revolucionario de DevOps llave en mano GRATUITO. 

Si usa Kubify, asegúrese de donar: [![](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donar?business=MSRFJHSGCKGCG&item_name=Kubify&currency_code=USD)


# Configuración


```

## New Account Config / ESP Configuración de cuenta nueva ##

# Create 3 AWS KMS Keys: / ESP Cree 3 claves de AWS KMS:
 # 1) kubify_secrets_dev
 # 2) kubify_secrets_stage
 # 3) kubify_secrets_prod
 
```

```

## Configure Env / ESP Configurar Env ##

export KUBIFY_DEBUG=1
export KUBIFY_CONTAINER_REGISTRY=ecr
export UNIQUE_COMPANY_ACRONYM=os
export EDITOR="subl -w "


## Local Testing / ESP Pruebas locales ##

./kubify up

#start entire infra locally !! / ESP iniciar toda la infraestructura localmente !!


kubify start-all

#cd into a specific service / ESP cd en un servicio específico


cd backend/example-node-svc

# start listening for code changes !! / ESP ¡Empiece a escuchar los cambios de código!


../../kubify start

```
complete `data` con pares ` key: value`, ejemplo:

```
data:

	EPIC_ENV_VARIABLE_9000: AWESOME_VERSIONED_SECRET_9000
metadata:

  name: example-django-simple-svc
type: Opaque

```
vas a querer guardar y cerrar esa ventana vim (wq!) .. en tu navegador o cartero GET / POST a tu servicio en ejecución https://example-node-svc.local.kubify.local
o a cualquiera de tus otros servicios https://[nombre de la carpeta de servicio].local.kubify.local

```
../../kubify secrets edit dev
```

¡kubify ahora escucha cualquier cambio de código en su servicio, así como también tiene EL RESTO DE INFRA FUNCIONANDO EN SU MÁQUINA! ..... y automáticamente (inmediatamente) sigue los registros de todos los servicios en el clúster .. MUY BUENO!!!

Cuando bifurque esto en su repositorio privado: recomiendo eliminar estas líneas del archivo .gitignore:

```
backend/*/secrets
backend/*/secrets/*
frontend/*/secrets
frontend/*/secrets/*
```

Si ha bifurcado este repositorio en su organización: debe eliminar esas 4 líneas en la parte superior del archivo .gitignore (para habilitar el control de versiones git cifrado de secretos, según lo diseñado).


# Impresionante



Compatible con Linux, Mac e incluso Windows !!


# Pero por qué Kubify


Porque los desarrolladores deberían poder centrarse en la codificación.

Porque la nube debe ser portátil y de código abierto.

Porque los desarrolladores deberían poder habilitar el registro de SO gratuito, apm, localstack, .. fácilmente.

Porque los desarrolladores deberían poder ejecutar toda la infraestructura en su computadora portátil, para probar rápidamente en un entorno real completo.

Porque los programadores son estrellas del rock. Debemos respetar a todos los codificadores que trabajan duro automatizando las cosas tanto como sea posible. Los codificadores necesitan piloto automático.

Este software permite a los desarrolladores probar toda la infraestructura localmente (en su totalidad) e implementarla en la nube (fácilmente), impulsando la calidad y la eficiencia #RAPIDTESTING #DEVEX #DEVOPS #DEVSECOPS #FREESOFTWARE

Esta herramienta le permite (con solo 2 comandos de terminal: `kubify up` & `kubify start-all` tener la infraestructura COMPLETA ejecutándose en su computadora portátil (sí, la infraestructura COMPLETA, increíble, revolucionaria), luego simplemente cd en el microservicio (cd en una carpeta backend / [] o frontend / []) carpeta en la que desea trabajar (luego ejecute kubify start) para iniciar pruebas rápidas (escucha los cambios de código, también ejecuta sus pruebas unitarias en cada guardado y configura automáticamente vscode para la configuración del punto de interrupción ) !!!!!!

Imagínese este nuevo mundo: ¡¡¡Un desarrollador en los primeros minutos (incluso el día 1) puede fácilmente ^^ (y luego puede concentrarse en su código real) !!!!!!!!!!!!!!!!!! !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

Ejecute el entorno real exacto localmente que está ejecutando en el entorno k8s implementado (para que pueda estar muy seguro de que su confirmación no romperá nada).

¡Esto es realmente importante en la industria de DevOps (así que contribuya)! Nuestros desarrolladores que trabajan arduamente deben obtener una solución llave en mano completa adecuada el día 1 que se haya probado en gran medida en la batalla. Piense en la nube, pero en código abierto. DevOps necesita evolucionar a DevOps 4.0, 4.5 y 5.0 rápidamente.

✅✅✅✅✅✅✅✅

Para las SRE (donde cada segundo de tiempo de actividad cuenta): Mult-Cloud también es importante. Realmente importante. ¡Piense en sitio / api / microservicio / mlops llave en mano de redundancia multi-nube!

Para Devs / DevOps / DevSecOps / DevEx: ¡Las pruebas locales (con TODA la infraestructura ejecutándose localmente a la perfección) deberían ser un clic de un botón (ESTA FUNCIÓN ESTÁ EN VIVO)!

✅✅✅✅✅✅✅✅



![FAST9000](./docs/img/README_md_imgs/fast.gif)



# Preguntas respondidas


Si desea aprender los comandos que ejecuta el contenedor de kubify: `KUBIFY_DEBUG = 1 kubify {args}`



Ejemplo:

```
KUBIFY_DEBUG=1 KUBIFY_CONTAINER_REGISTRY=ecr UNIQUE_COMPANY_ACRONYM=os kubify up
```

NOTE: UNIQUE_COMPANY_ACRONYM debe ser único


# Ejemplos de edición de secretos


Para usar el editor predeterminado:

```
cd backend/be-svc
kubify secrets create dev
```

Para utilizar el editor alternativo:

```
brew install cask sublime-text
export EDITOR="subl -w"
cd backend/be-svc
kubify secrets create dev
```

# Cómo contribuir al repositorio de SO


https://github.com/willyguggenheim/kubify es el repositorio oficial del sistema operativo (combinación de las versiones 2015 y 2017 del repositorio kubify_com del sistema operativo de Willy y refactorizado en 2021 al repositorio oficial del sistema operativo, por lo que este es el principal repositorio oficial al que contribuir)

Si encuentra algún error, ha creado y agregado características nuevas interesantes, habrá un PR.

Si es nuevo en el código abierto, este enlace lo ayudará a comenzar con su primer RP en un repositorio de SO.

Para obtener más información sobre el flujo de revisión de relaciones públicas de contribución: https://github.com/firstcontributions/first-contributions



# Dime de nuevo porque


Porque DevOps ama a los desarrolladores que trabajan muy duro y a los Científicos de Datos geniales (así que hagámoslo más fácil para ellos).



#Calibración de esta herramienta 


si un desarrollador en el día 1 puede hacer todas estas cosas sin el soporte de DevOps, entonces hemos tenido éxito:

1) Ejecutar toda la infraestructura en la estación de trabajo coincidiendo exactamente con la forma en que se ejecuta en producción con 1 comando.

2) Realice un cambio de 1 línea en un servicio iniciando la depuración de un debug ide completo con 1 comando, pruébelo con 1 comando, pruébelo unitario con 1 comando y luego impleméntelo cambiando 1 archivo de entorno (¡ESTA FUNCIÓN ESTÁ ACTIVA!)

3) docs es autosuficiente sin intervención manual (corrige todos los casos extremos), hazlo simplemente perfecto (es por eso que tus contribuciones de codificación a este mismo repositorio son SUPER importantes, 🤘 increíble genio de las pruebas rápidas 🤘 y codificador que trabaja duro 🤘 !!!!!!!!!)
 


![YES9000](./docs/img/README_md_imgs/so-much-yes.gif)



Creo que todos sabemos qué tipo de justicia sería útil para nuestros desarrolladores que trabajan duro.

De esta manera, un desarrollador en el día 1 puede ser efectivo, en funcionamiento, y todos los desarrolladores pueden probar rápidamente toda la infraestructura localmente y tener mucha confianza en la calidad de sus implementaciones (se ejecuta de la misma manera localmente que en el entorno implementado).

Los marcos de prestación de servicios son lenguajes de programación. Esta es una descripción de 'mejores prácticas' (marco automatizado llave en mano) para SDLC sin problemas, para cubrir la mayoría de los puntos débiles en DevEx, producir código de alta calidad, habilitar pruebas rápidas, habilitar un autoservicio rápido para desarrolladores y hacer que todo su trabajo sea duro desarrolladores super felices!

Kubernetes puede ser complejo (vea los ejemplos a continuación), así que vamos a automatizar + organizar y, a su vez, simplificarlo. ¡Vamos a Kubificarlo!

https://k8s.af/

https://news.ycombinator.com/item?id=26106080

https://www.trendmicro.com/en_us/research/21/b/threat-actors-now-target-docker-via-container-escape-features.html

https://news.ycombinator.com/item?id=26121877



# Notas importantes


El entorno "dev" es el mismo entorno cuando se ejecuta localmente que el entorno implementado (tanto el desarrollador local como el real implementado k8s env usan el archivo "environment / dev.yaml", con un diseño cuidadoso)


# Conceptos clave

1 yaml por servicio

Sí, lo escuchaste bien, finalmente está aquí, 1 archivo yaml en total, con una sintaxis mínima (que aún permite patrones de uso avanzados) que los desarrolladores y devops pueden mantener fácilmente, ¡10 veces más fácil !!!!!!!!!!!!

1 yaml por entorno

dev.yaml = entorno "dev" implementado "local" y real mientras comparten un archivo, mediante un diseño cuidadoso de DevEx ... sí, me escuchaste bien, ejecuta todos los desarrolladores en tu computadora portátil también y haz una prueba rápida localmente en 2 en total de 1 comandos desde cero, incluso el día 1, ¡10 veces más fácil!

dev.yaml = para local y dev env (ambos)

1 carpeta para servicios backend.

1 carpeta para servicios frontend.

El controlador de ingreso cifra el tráfico entre servicios.

La automatización del controlador de entrada cifra el tráfico entre el host y los servicios.

El controlador de ingreso genera un certificado sobre la marcha y lo agrega a sus certificados de confianza en el host.

Los servicios escuchan automáticamente los cambios de código al ejecutar `kubify start`

¡Kubify generará AUTOMÁTICAMENTE un Dockerfiles para usted, detectando automáticamente el idioma en el que ha escrito el servicio (si no hay Dockerfile.dev o / y Dockerfile.build)!

opciones para la ubicación de Dockerfile: 

A) {{app_dir}}/Dockerfile.dev y {{app_dir}}/Dockerfile.build (ambos necesitan usar un dockerfile personalizado).

B) no Dockerfile * en app_dir (porque crea uno para usted basado en el idioma)!!!

.. para que esos patrones de acceso de DevSecOps nunca se mezclen en un yaml

Puro amor de los desarrolladores de DevEx ...

El objetivo de esta herramienta es facilitar Kubernetes para los desarrolladores. 

Un desarrollador (o devops) solo necesita completar un archivo yaml para incorporar cualquier servicio.

Las bases de datos están automatizadas con KubeDB y controladas desde el mismo archivo yaml.

Los CRON se definen en el mismo yaml.

La configuración de inicialización / migración también se define en el mismo archivo yaml.

Los valores predeterminados están en su lugar, en caso de que un desarrollador quiera proporcionar un yaml mínimo.

Los secretos se versionan de forma segura en el mismo repositorio mono. Cada vez que un desarrollador ejecuta `kubify secrets edit dev`, AWS IAM primero verifica si el usuario todavía tiene acceso.

La carpeta Entornos tiene 1 archivo yaml por entorno controlando dónde se despliega.

Un desarrollador puede controlar qué etiqueta de versión de servicio, qué etiqueta de grupo secreta git o commit sha usar, y qué etiqueta de configuración git o commit sha usar dónde. Revertir secretos, versión de servicio y versión de configuración es tan fácil como un PR de 3 líneas en GitHub.


El etiquetado automático, la agrupación de artefactos, la construcción de contenedores, las implementaciones y los flujos de lanzamiento se implementan mediante GitHub Actions CICD y se desarrollan dentro del mismo repositorio mono.

Route53 está controlado por la integración de Kubernetes, para implementaciones comprobadas en la nube Blue-Green.


Los cambios de Terraform se realizan en una carpeta de infraestructura y son visibles / controlados con 2 aprobadores que utilizan la integración de Atlantis y GitHub. Todos los recursos de AWS están automatizados para implementar la misma pila (como su computadora portátil) en la nube (EKS…).


Cuando un desarrollador quiere ejecutar todos los servicios en su computadora portátil, todo lo que necesita para ejecutar es kubify run-all. Kubernetes que usa Docker Desktop (Mac / Linux / Windows) se instalará / reinstalará / configurará / reconfigurará a sí mismo, extraerá los últimos contenedores enviados e iniciará la pila, sin usar muchos recursos (la máquina del desarrollador aún es rápida). Cuando un desarrollador quiere editar el código de un servicio específico, lo está desarrollando en un entorno implementado automáticamente en su portátil (Kube DBs, Queues, Crons, Services, ... y todo). La recarga de código en vivo se utiliza para el desarrollo y las pruebas de ritmo rápido.


En general, la herramienta es revolucionaria y una receta sólida para la automatización completa de Kubernetes, que encajaría en la mayoría de las situaciones, haría que los desarrolladores fueran súper eficientes y reduciría la carga de DevOps para la ingeniería de versiones.All in all, the tool is revolutionary and is a solid prescription for full Kubernetes automation, that would fit in most situations, make developers super efficient and reduce the burden on devops for release engineering.


La conclusión es que un desarrollador el día 1 puede mostrar toda la pila en su computadora portátil, implementarla en entornos de manera visible (en un simple PR), ¡y la incorporación se convierte en una brisa!


¡Hagamos de kubernetes la herramienta devops más importante del planeta (porque su portabilidad e interfaces son ❤️ puro amor ❤️)!


¡Hagamos que nuestros desarrolladores que trabajan duro estén súper felices juntos (porque todas las cosas de DevOps se automatizarán tanto como sea posible)!


¡Automaticemos juntos tanto como sea posible (cuantos más contribuyentes, mejor será devops 4.0)!


¡Hagamos que DevOps 4.0 sea portátil, flexible, automatizado y de código abierto!


¡Construyamos DevOps 4.0 juntos!


La versión 1 de Kubify está activa y en master branch. 


Avísame si funciona bien en tus dispositivos Apple y Linux.


Esto es lo que se siente correr `kubify up`:



![FIXED9000](./docs/img/README_md_imgs/bugs-fixed-v1-ready.gif)



Quires correr? Corre `kubify up` !Hey, eso rima!



¡¡¡Así que construyamos en cosas increíbles juntos !!!



![AUTOMATION9000](./docs/img/README_md_imgs/iron-person.gif)


Un agradecimiento especial a las interfaces de código abierto totalmente automatizadas (automatización idéntica local e implementada), como KubeDB y Kafka.

https://github.com/operator-framework/awesome-operators


En el mundo de Kubernetes, esto es verdaderamente revolucionario, único en su tipo (debido a las automatizaciones de pruebas locales que combinan las automatizaciones del entorno implementadas llave en mano y las interfaces portátiles híbridas de k8s) y fue muy divertido de construir.


![LEVELOVER9000](./docs/img/README_md_imgs/level-up.gif)


¡Esta es la era de la nube portátil totalmente automatizada de código abierto auto-devops devex-first devsecops-first!

Muy bien, ¿quién está listo para el futuro inevitable de DevOps y desarrollo de software?

`print laymans terms / imprimir términos de laicos`: Esto es Auto-Pilot para DevOps. Haga felices a sus DevOps, DevEx, DevSecOps y especialmente a sus desarrolladores, permitiéndoles ser súper productivos, utilizando turn kuy, soluciones totalmente automatizadas que les permiten probar el software localmente (en la misma estación de trabajo que usan actualmente o en un sidecar). estación de trabajo, si, por ejemplo, necesitan cargas de trabajo de GPU) de la misma manera exacta en que se ejecutan en su infraestructura implementada (nube, local o un probador de estación de trabajo lateral del automóvil nuc). Permita que sus desarrolladores tengan una solución DevOps llave en mano totalmente automatizada, permitiendo que sus devops se centren en la seguridad, los clientes y, especialmente, en kubify. 

Ahorre enormes costos en la nube. Ejecútelo todo en su estación de trabajo. Ejecute múltiples entornos en su estación de trabajo (piense en el futuro de la computación periférica cicd local asincrónica en el que viviremos).

La sensación que tienen sus desarrolladores y devs cuando toda la infraestructura es portátil y se ejecuta en su estación de trabajo (para realizar pruebas rápidas en un entorno real completo):


![OVER9000](./docs/img/README_md_imgs/over-9000.gif)


`print laymans terms | summary /  imprimir términos laicos | resumen`: Esto hace que sus DevOps, equipos de seguridad y especialmente sus desarrolladores estén muchas veces más felices.


![SERIOUSLYDEEPLYOVER9000](./docs/img/README_md_imgs/the-feels.gif)


¿Aún necesitas motivación ?: El desarrollador y creador principal, Willy Guggenheim, trabaja junto a 9 pequeños y tranquilos chihuahuas, ama el MetalCore, el pop latino, el ambiente, la música clásica, el EDM y especialmente el hip hop.


Todavía necesito motivación (ES FÁCIL QUE SE PEGUE):
https://www.youtube.com/watch?v=7m0n8h8b89M !!
 
 
Kubify = El código abierto, gratuito, portátil, totalmente automatizado, habilitado para DR, Turn Key Head First Clou que le permite ejecutar toda su infraestructura localmente de la misma manera que se implementa en la nube.

![FUTUREOFDEVOPS9000](./docs/img/README_md_imgs/the-future.gif)

Hecho por desarrolladores, para desarrolladores

#AUTOPILOTFORDEVOPS

#PILOTOAUTOMÁTICOPARADEVOPS

#STAYINSPIRATIONAL

#MANTENGALAINSPIRACION

#FREESOFTWARE

#THEFUTURE

#DEVLOVE

#DEVEX

💻
