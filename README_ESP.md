💻 TRADUCCIÓN EN ESPAÑOL

# Descripción
 
Kubify es una herramienta CLI (interfaz de línea de comandos) para administrar el ciclo de vida de desarrollo e implementación de microservicios.
 
# Configuración

```

## Configure Env ##



## Setup ##

ln -sf $(pwd)/kubify/tools/kubify/cli/kubify /usr/local/bin/kubify # or export PATH=$PATH:$(pwd)/tools/kubify/cli

export KUBIFY_DEBUG=1
export KUBIFY_CONTAINER_REGISTRY=ecr
export UNIQUE_COMPANY_ACRONYM=os

#install/configure/re-configure fully automated with 1 command
kubify up



## Local Testing ##

#start all services locally (entire infra running locally)
kubify start-all 

#cd into a specific service
cd backend/backend-svc

#listens for code changes, shows logs, runs unit tests (on each code save), opens and auto-configures IDE
kubify start

```

# Pero por qué

Esta herramienta le permite (con solo 2 comandos de terminal: kubify up && kubify start-all) tener la infraestructura COMPLETA ejecutándose en su computadora portátil (sí, la infraestructura COMPLETA, increíble, revolucionaria), luego simplemente cd en el microservicio (cd en una carpeta backend / [ ] o frontend / [ ]) carpeta en la que desea trabajar (luego ejecute kubify start) para iniciar pruebas rápidas (escucha los cambios de código, también ejecuta sus pruebas unitarias en cada guardado y configura automáticamente vscode para la configuración del punto de interrupción)

Imagínese este nuevo mundo: ¡¡¡Un desarrollador en los primeros minutos (incluso el día 1) puede hacer fácilmente ^^ (y luego puede concentrarse en su código real) !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!


Ejecute el entorno exacto que está ejecutando en el entorno k8s (Kubernetes) implementado localmente (para que pueda estar muy seguro de que su confirmación no romperá nada, prueba rápida y que se ve bonito).


✅✅✅✅✅✅✅✅


Esto es realmente importante en la industria de DevOps (así que contribuya). Nuestros desarrolladores deben obtener una solución llave en mano completa (full turnkey)  adecuada desde el día 1 que esté probada en batalla. Piense en la nube, pero en código abierto. DevOps necesita evolucionar a DevOps 4.0 y rápido.


✅✅✅✅✅✅✅✅


Las pruebas locales (con TODA la infraestructura ejecutándose localmente perfectamente) deberían ser un clic de un botón (ESTA FUNCIÓN ESTÁ EN VIVO)!!


✅✅✅✅✅✅✅✅


![FAST9000](./docs/img/README_md_imgs/fast.gif)]


# Tenga en cuenta

Compatible con Linux, Mac y Windows (con WSL2). 
Si está en Windows, utilice Ubuntu para Windows (en la tienda de aplicaciones de Windows) para ejecutar este.
 
# Preguntas respondidas

Si desea aprender los comandos que ejecuta el contenedor de kubify:

`KUBIFY_DEBUG=1 kubify {args}`

Ejemplo:  `KUBIFY_DEBUG=1 KUBIFY_CONTAINER_REGISTRY=ecr UNIQUE_COMPANY_ACRONYM=os kubify up`
	- NOTA: UNIQUE_COMPANY_ACRONYM debe ser único

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

Porque DevOps ama a los desarrolladores que trabajan muy duro y a los Científicos de Datos, son geniales (así que hagámoslo fácil para ellos).



Calibración de esta herramienta: si un desarrollador en el día 1 puede hacer todas estas cosas sin el soporte de DevOps, entonces hemos tenido éxito:

1) Ejecutar toda la infraestructura en la estación de trabajo coincidiendo exactamente con cómo se ejecuta en producción con 1 comando.


2) Realice un cambio de 1 línea en un servicio iniciando la depuración de un debug IDE completo con 1 comando, pruébelo con 1 comando, pruébelo unitario con 1 comando y luego implementarlo cambiando 1 archivo de entorno (¡ESTA FUNCIÓN ESTÁ ACTIVA!)


 3) docs es autosuficiente sin intervención manual (arregle todos los casos extremos), hágalo perfecto (por eso sus contribuciones de codificación a este mismo repositorio son SUPER importantes, 🤘increíble genio de las pruebas🤘 rápidas y codificador que trabaja duro !!! )


![YES9000](./docs/img/README_md_imgs/so-much-yes.gif)
 

Creo que todos sabemos qué tipo de justicia sería útil para nuestros desarrolladores que trabajan duro.

De esta manera, un desarrollador en el día 1 puede ser efectivo, en funcionamiento, y todos los desarrolladores pueden probar rápidamente toda la infraestructura localmente y tener mucha confianza en la calidad de sus implementaciones (se ejecuta de la misma manera localmente que en el entorno implementado).

Los marcos de prestación de servicios son lenguajes de programación. Esta es una descripción de 'mejores prácticas' (marco automatizado turn key / automated turn-key framework) para SDLC sin problemas, para cubrir la mayoría de los puntos débiles en DevEx, producir código de alta calidad, habilitar pruebas rápidas, habilitar un autoservicio rápido para desarrolladores y hacer que todo su trabajo sea duro desarrolladores super felices.

Kubernetes puede ser complejo (vea los ejemplos a continuación), así que vamos a automatizar + organizar y a su vez, simplificarlo. ¡Vamos a Kubificarlo!

https://k8s.af/

https://news.ycombinator.com/item?id=26106080

https://www.trendmicro.com/en_us/research/21/b/threat-actors-now-target-docker-via-container-escape-features.html
https://news.ycombinator.com/item?id=26121877


# Notas importantes

El entorno "dev" es el mismo entorno cuando se ejecuta localmente que el entorno implementado (tanto el desarrollador local como el real implementado k8s (Kubernetes) env usan el archivo "environment / dev.yaml", con un diseño cuidadoso)

# Conceptos clave

1 yaml por servicio

Sí, lo escuchaste bien, finalmente está aquí, 1 archivo yaml en total, con una sintaxis mínima (pero también permite patrones de uso avanzados, todavía solo 1 archivo devops total por servicio (que los desarrolladores y devops pueden mantener fácilmente, ¡10 veces más fácil)!!!
 
1 yaml por entorno

dev.yaml = entorno "dev" implementado "local" y real (comparten un archivo, por diseño, sí, me escuchaste bien, ejecuta todos los dev en tu computadora portátil también y haz una prueba rápida localmente en 2 un total de 1 comandos desde cero, incluso el día 1, ¡¡¡10 veces más fácil !!!)

1 carpeta para servicios backend

1 carpeta para servicios frontend

.. para que esos patrones de acceso a DevSecOps no se mezclen nunca en un yaml
Amor puro de los desarrolladores de DevEx ...

El objetivo de esta herramienta es hacer que Kubernetes sea fácil para los desarrolladores.

Un desarrollador (o devops) solo tiene que completar un archivo yaml para incorporar cualquier servicio.

Las bases de datos se automatizan con KubeDB y se controlan desde el mismo archivo yaml.

Los cron se definen en el mismo yaml.

Los cron se definen en el mismo yaml.

La configuración de inicialización / migración también se define en el mismo yaml.

Los valores predeterminados están en su lugar, en caso de que un desarrollador quiera proporcionar un yaml mínimo.



Los secretos se versionan de forma segura en el mismo repositorio mono. Cada vez que un desarrollador ejecuta `kubify secrets edit dev`, AWS IAM primero verifica si el usuario todavía tiene acceso.

La carpeta Entornos tiene 1 archivo yaml por entorno que controla qué se implementa y dónde.

Un desarrollador puede controlar qué etiqueta de versión del servicio, qué secretos empaquetan la etiqueta git o que commit sha usar y qué etiqueta git de configuración o que commit sha usar. Revertir secretos, versión de servicio y versión de configuración es tan fácil como un PR de 3 líneas en GitHub.



El etiquetado automático, la agrupación de artefactos, la construcción de contenedores, las implementaciones y los flujos de liberación se implementan mediante GitHub Actions CICD y se desarrollan dentro del mismo repositorio mono.

Route53 se controla mediante la integración de Kubernetes, para implementaciones probadas en la nube Blue-Green.
Los cambios de Terraform se realizan en una carpeta de infraestructura y son visibles / controlados con 2 aprobadores que utilizan la integración de Atlantis y GitHub. 
Todos los recursos de AWS están automatizados para implementar la misma pila (como su computadora portátil) en la nube (EKS).

Cuando un desarrollador quiere ejecutar todos los servicios en su computadora portátil, todo lo que necesita para ejecutar es:`kubify run-all`. Kubernetes que usa Docker Desktop (Mac / Linux / Windows) se instalará / reinstalará / configurará / reconfigurará a sí mismo, extraerá los últimos contenedores insertados e iniciará la pila, sin usar muchos recursos (la máquina del desarrollador sigue siendo rápida). Cuando un desarrollador desea editar el código de un servicio específico, lo está desarrollando en un entorno implementado automáticamente en su computadora portátil (Kube DBs, Queues, Crons, Services, ... y todo). La recarga de código en vivo se utiliza para desarrollar y probar a un ritmo rápido.



Con todo, la herramienta es revolucionaria y es una receta sólida para la automatización completa de Kubernetes, que encajaría en la mayoría de las situaciones, haría que los desarrolladores fueran súper eficientes y reduciría la carga de DevOps para la ingeniería de versiones.



El resultado final es que un desarrollador en el día 1 puede mostrar toda la pila en su computadora portátil, implementarla en entornos de manera visible (en un simple PR) y ¡la incorporación se convierte en una brisa!



¡Hagamos de kubernetes la herramienta devops más importante del planeta (porque su portabilidad y las interfaces son ❤️ puro amor ❤️)!

¡Hagamos que nuestros desarrolladores que trabajan duro estén súper felices juntos (porque todas las cosas de DevOps se automatizarán tanto como sea posible)!

¡Automaticemos juntos tanto como sea posible (cuantos más contribuyentes, mejor será devops 4.0)!

¡Hagamos que DevOps 4.0 sea portátil, flexible, automatizado y de código abierto!

¡Construyamos DevOps 4.0 juntos!



La versión 1 de Kubify está activa y en la rama maestra.

Compartan si funciona bien en tus dispositivos Apple y Linux.

Esto es lo que se siente correr `kubify up`:
 
 
 
![FIXED9000](./docs/img/README_md_imgs/bugs-fixed-v1-ready.gif)


¿Quieres prisa? Correr `kubify up` ¡Oye, eso rima!


¡¡¡Así que construyamos cosas increíbles juntos !!!



![AUTOMATION9000](./docs/img/README_md_imgs/iron-person.gif)



Un agradecimiento especial a las interfaces de código abierto totalmente automatizadas (automatización idéntica local e implementada), como KubeDB y KubeMQ.



![LEVELOVER9000](./docs/img/README_md_imgs/level-up.gif)
  
 
En el mundo de Kubernetes, esto es verdaderamente revolucionario, único en su tipo (debido a las automatizaciones de pruebas locales que combinan las automatizaciones del entorno implementadas llave en mano (turnkey) y las interfaces portátiles híbridas de k8s(Kubernetes)) y fue muy divertido de construir.


¡Esta es la era de la nube portátil totalmente automatizada de código abierto auto-devops devex-first devsecops-first!

Muy bien, ¿quién está listo para el futuro inevitable de DevOps y desarrollo de software?

`print laymans terms/ imprimir términos de laicos`:Esto es Auto-Pilot para DevOps. Haga felices a sus DevOps, DevEx, DevSecOps y especialmente a sus desarrolladores, permitiéndoles ser súper productivos, utilizando turn kuy, soluciones totalmente automatizadas que les permiten probar el software localmente (en la misma estación de trabajo que usan actualmente o en una estación de trabajo lateral, si, por ejemplo, necesitan cargas de trabajo de GPU) de la misma manera exacta en que se ejecutan en su infraestructura implementada (nube, local o un probador de estación de trabajo lateral para automóvil). Permita que sus desarrolladores tengan una solución DevOps llave en mano totalmente automatizada, permitiendo que sus devops se centren en la seguridad, los clientes y, especialmente, en kubify.

Ahorre enormemente en los costos de la nube. Ejecútelo todo en su estación de trabajo. 

Ejecute varios entornos en su estación de trabajo (piense en el futuro de la informática de borde CICD local asincrónica en el que viviremos).
 
 
![OVER9000](./docs/img/README_md_imgs/over-9000.gif)
 
 
La sensación que tienen sus desarrolladores y devs cuando toda la infraestructura es portátil y se ejecuta en su estación de trabajo (para realizar pruebas rápidas en un entorno real completo):

`print laymans terms | summary / imprimir términos laicos | resumen`:Esto hace que sus DevOps, equipos de seguridad y, especialmente, sus desarrolladores estén muchas veces más felices.

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

