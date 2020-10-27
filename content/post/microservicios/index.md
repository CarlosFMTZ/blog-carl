---
title: "Arquitectura de microservicios"
date: 2020-03-22
tags: ["microservicios", "java", "arquitectura", "tutorial"]
categories: ["microservicios", "arquitectura"]
description: "Tutorial de arquitectura de microservicios: todo lo que necesita para comenzar"
draft: false
---

# 

La arquitectura de microservicios es una de las tendencias de arquitectura de software más discutidas en este momento, y ha cambiado para siempre la forma en que se crean las aplicaciones empresariales. En lugar del lento y complejo enfoque monolítico del pasado, los desarrolladores y las empresas de todo el mundo están recurriendo a la arquitectura de microservicios para simplificar y escalar sus estructuras. De hecho, incluso compañías como Amazon, Netflix, Spotify y Uber han hecho la transición.

Si desea comenzar con Microservicios o simplemente tiene curiosidad sobre el debate que lo rodea, está en el lugar correcto. Hoy, lo guiaré a través de todo lo que necesita saber sobre Microservicios, desde ejemplos del mundo real hasta patrones de arquitectura y más. Cubriremos lo siguiente:

¿Qué es la arquitectura de microservicios?
- Ventajas y desventajas
- Microservicios y Docker
- Stacks tecnológicos y patrones de arquitectura
- Guía de recursos

¡Empecemos!

¿Qué es la arquitectura de microservicios?
No existe una definición universal del término microservicios. La definición más simple de microservicios, también llamada arquitectura de microservicios, es un estilo arquitectónico que estructura una aplicación que utiliza servicios poco acoplados. Estas colecciones o módulos se pueden desarrollar, implementar y mantener de forma independiente.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--dLutT_pe--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/bajsjx8nfugicl8pssnf.png)

![](https://res.cloudinary.com/practicaldev/image/fetch/s--nyxrwl1N--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/t4m9isito1l0trhq4qr6.png)
Operan a una velocidad mucho más rápida y confiable que las aplicaciones tradicionales complejas y monolíticas. Usando arquitecturas de microservicio, una organización de cualquier tamaño puede desarrollar pilas de tecnología adaptadas a sus capacidades.

El uso de microservicios ofrece muchos beneficios tangibles, que discutiremos más adelante, pero aún existe cierta controversia sobre si las empresas deberían cambiar de una arquitectura monolítica a una de microservicios. Examinemos la diferencia entre los dos para entender el debate.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--pmzshbmT--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/wop9t4jjyg55c7f6e6ep.png)
Monolítico vs. Microservicios
La arquitectura monolítica es la forma tradicional de construir y desplegar aplicaciones. Esta estructura se basa en el concepto de una única unidad indivisible, que incluye el lado del servidor, el lado del cliente y la base de datos. Todas las facetas están unificadas y administradas como una sola unidad y base de código. Esto significa que cualquier actualización debe realizarse en la misma base de código, por lo que debe modificarse toda la pila. A medida que las aplicaciones monolíticas escalan, pueden volverse bastante complejas, por lo que el desarrollo general es generalmente más largo.

Una arquitectura de microservicios, por otro lado, descompone esa unidad en unidades independientes que funcionan como servicios separados. Esto significa que cada servicio tiene su propia lógica y base de código. Se comunican entre sí a través de API (interfaces de programación de aplicaciones).

Entonces, ¿qué arquitectura debes elegir? Vamos a desglosarlo.

Elegir una arquitectura monolítica
Si tu empresa es un equipo pequeño. De esta manera, no tiene que lidiar con la complejidad de implementar una arquitectura de microservicio.

Si quieres un lanzamiento más rápido. La arquitectura monolítica requiere menos tiempo para iniciarse. Este sistema requerirá más tiempo más adelante para actualizar su sistema, pero el inicio inicial es más rápido.

Elegir una arquitectura de microservicios
Si quieres desarrollar una aplicación más escalable. Escalar una arquitectura de microservicios es mucho más fácil. Se pueden agregar nuevas capacidades y módulos con mucha facilidad y rapidez.
Si su empresa es más grande o planea crecer. El uso de microservicios es excelente para una empresa que planea crecer, ya que la arquitectura de microservicios es mucho más escalable y más fácil de personalizar con el tiempo.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--h7cHGoIP--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/1v7rcl7myqnrt2vkdz58.png)

Ventajas e inconvenientes de los microservicios.
Existen varias razones por las que una arquitectura de microservicios es una mejor opción para su empresa. Analicemos los beneficios más notables y luego examinemos algunos de los inconvenientes.

Beneficios
Mejora la escalabilidad y la productividad.
Los grandes equipos a menudo tienen que trabajar juntos en proyectos complejos. Con microservicios, los proyectos se pueden dividir en unidades más pequeñas e independientes. Esto significa que los equipos pueden actuar independientemente con respecto a la lógica de dominio, lo que minimiza la coordinación y el esfuerzo. Además de eso, los equipos responsables de cada microservicio pueden tomar sus propias decisiones tecnológicas según sus necesidades.

Por ejemplo, la estructura interna de cada unidad o contenedor no importa mientras la interfaz funcione correctamente. Por lo tanto, cualquier lenguaje de programación puede usarse para escribir un microservicio, de modo que el equipo responsable pueda seleccionar el mejor idioma para sus compañeros de equipo.

Se integra bien con sistemas heredados
Los sistemas monolíticos son difíciles de mantener. Muchos sistemas heredados están mal estructurados, mal probados o dependen de tecnologías obsoletas. Afortunadamente, los microservicios pueden funcionar junto con los sistemas heredados para mejorar el código y reemplazar las partes antiguas del sistema. La integración es fácil y puede resolver muchos de los problemas que hacen que los sistemas monolíticos sean algo del pasado.

Desarrollo sostenible
Las arquitecturas de microservicios crean sistemas que pueden mantenerse a largo plazo ya que las diversas partes son reemplazables. Esto significa que un microservicio puede reescribirse fácilmente sin comprometer todo el sistema. Siempre que las dependencias entre microservicios se gestionen de manera adecuada, se pueden hacer cambios fácilmente para optimizar las necesidades y el rendimiento del equipo.

Funcionalidad cruzada
Los microservicios son los mejores para equipos distribuidos. Si tiene equipos en todo el mundo o varias divisiones, los microservicios le otorgan las libertades y la flexibilidad necesarias para trabajar de forma autónoma. Se pueden tomar decisiones técnicas rápidamente que se integran con otros servicios en un instante. La funcionalidad cruzada nunca ha sido tan fácil.

Inconvenientes
La implementación requiere más esfuerzo
La operación de un sistema de microservicio a menudo requiere más esfuerzo, ya que hay más unidades desplegables que deben implementarse y monitorearse. Los cambios en las interfaces deben implementarse de modo que todavía sea posible una implementación independiente de microservicios individuales.

La prueba debe ser independiente
Como todos los microservicios deben probarse juntos, un microservicio puede bloquear la etapa de prueba y evitar el despliegue de los otros microservicios. Hay más interfaces para probar, y las pruebas deben ser independientes para ambos lados de la interfaz.

Difícil de cambiar múltiples microservicios
Los cambios que afectan a múltiples microservicios pueden ser más difíciles de implementar. En un sistema de microservicio, los cambios requieren varias implementaciones coordinadas.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--QNiSxSBi--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/9slt3h9vwlj1fn9kawxj.png)

Microservicios y Docker
Docker y Microservicios son casi sinónimos. Los microservicios deben ser unidades independientes escalables y desplegables por separado. Pero, ¿qué pasa si crea múltiples microservicios para su aplicación? Docker es una solución ligera para implementar microservicios. Un microservicio puede empaquetarse en una imagen Docker y aislarse como un contenedor Docker. De esta manera, puede crear una aplicación que sea independiente de su entorno de host.

En lugar de tener una máquina virtual completa propia, los contenedores Docker comparten el núcleo del sistema operativo en el host Docker. Los procesos de los contenedores aparecen en la tabla de procesos del sistema operativo en el que se ejecutan los contenedores Docker.

Para usar Docker con microservicios, debe crear imágenes de Docker a través de los archivos nombrados Dockerfile. Los Dockerfiles son fáciles de escribir, por lo que implementar software puede ser fácil. Eche un vistazo a un ejemplo de un Dockerfile para un microservicio Java.
FROM openjdk:11.0.2-jre-slim
COPY target/customer.jar .
CMD /usr/bin/java -Xmx400m -Xms400m -jar customer.jar
EXPOSE 8080
¿Quieres aprender más sobre Docker? Echa un vistazo al curso educativo sobre los conceptos básicos de Docker y Kubernetes

Un sistema de microservicio típico contiene múltiples contenedores Docker. La coordinación de un sistema de múltiples contenedores Docker requiere configuraciones para la red virtual. Los contenedores deben poder encontrarse entre sí para comunicarse. El entorno Docker Compose puede contactar a otro servidor a través de un enlace, que ofrece un sistema de descubrimiento de servicios.

Sigue aprendiendo.
Aprenda la arquitectura de microservicios sin desplazarse por videos o documentación. Los cursos educativos basados en texto son fáciles de leer y cuentan con entornos de codificación en vivo, lo que hace que el aprendizaje sea rápido y eficiente.

Una introducción a los principios y conceptos de microservicio

![](https://res.cloudinary.com/practicaldev/image/fetch/s--l_7swGIJ--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/4lzkoitaf72dif7gjwrk.png)

Pilas tecnológicas y patrones de arquitectura
Una cosa es entender cómo funciona la microarquitectura y otra es construirla e implementarla. Es por eso que queremos centrarnos en las diversas tecnologías disponibles para un sistema completo de microservicios. Veamos algunas pilas tecnológicas, patrones y diseños diferentes para crear una arquitectura ejecutable de microservicios.

Decisiones de arquitectura micro y macro
Es aconsejable dividir su arquitectura en micro y macro arquitectura. La microarquitectura involucra todas las decisiones tomadas para cada microservicio. La macro arquitectura involucra todas las decisiones tomadas a nivel global que se aplican a todos los microservicios.

Es posible extender el concepto de micro y macro arquitectura a las decisiones técnicas. Las decisiones técnicas se pueden tomar en el marco de la macro o micro arquitectura. Por ejemplo, eche un vistazo a las decisiones técnicas que se tomarán a nivel micro y macro para una base de datos:

Micro: cada microservicio puede tener su propia instancia de la base de datos. Si las bases de datos se definieron en la microarquitectura, un bloqueo de una base de datos solo conducirá al bloqueo de un microservicio. Esto hace que toda la aplicación sea mucho más robusta.

Macro: la base de datos también se puede definir como parte de la arquitectura macro. Múltiples microservicios no deben compartir un esquema de base de datos.


![](https://res.cloudinary.com/practicaldev/image/fetch/s--n7sVxXfB--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/qgoickv3qvtr7zigyitf.png)

Sistemas autónomos
Un sistema autónomo (SCS) es un tipo de arquitectura de microservicio que especifica los elementos de una arquitectura macro. Esto significa que no representan todo el sistema. Dado que un SCS es autónomo, proporciona todo lo que necesita para implementar una parte de la lógica de dominio, como datos de registro y una interfaz de usuario. Los SCS también tienen una API opcional.

Por ejemplo, un SCS para un pago de microservicio almacenaría información relevante para ese pago como un contexto acotado. También implementaría la interfaz de usuario para mostrar el historial de pagos, y los datos sobre los clientes se replicarían desde otros SCS.

Piense en esto como una colección de mejores prácticas; Los SCS proporcionan reglas precisas basadas en patrones establecidos, ofreciendo un punto de referencia sobre cómo construir una arquitectura de microservicio. Todas estas reglas aseguran que un SCS implemente un dominio, por lo que una característica adicional solo cambia un SCS.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--8oRirkhV--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/rdrc5zkv4yvuy960dbl5.png)
Podemos pensar en un SCS como una arquitectura de microservicio porque se puede implementar de forma independiente y dividir un sistema en aplicaciones web independientes. De hecho, un SCS puede incluso dividirse en varios microservicios. Se diferencian de los microservicios en tres formas principales: son más grandes que los microservicios; se centran en el acoplamiento flojo; deben tener una interfaz de usuario.

Puede obtener más información sobre SCS aquí

Integración Frontend
Los microservicios también se pueden integrar con una interfaz web. Dividir el frontend en diferentes módulos ayuda a resolver algunos de los problemas que surgen de tratarlo como un monolito. Una interfaz modular se compone de microservicios desplegables por separado. Esto puede traer muchos beneficios a su interfaz.

Por ejemplo, un frontend modularizado puede tener una lógica de dominio independiente, y un cambio en el dominio puede implementarse simplemente modificando un solo microservicio. Para combinar una interfaz separada, deben integrarse, por lo que es necesario un sistema de integración.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--GKhh6oMa--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/tjicr6h4vo6v07i1z5nz.png)
Esto se puede lograr a través de enlaces, donde una interfaz muestra un enlace que otra interfaz lee y maneja. Esto también se puede lograr a través de redireccionamientos, por ejemplo, cómo OAuth2 maneja la integración frontend. Los redireccionamientos combinan la transferencia de datos con la integración frontend.

Sin embargo, hay algunas excepciones cuando una interfaz se debe implementar como un monolito. Por ejemplo, las aplicaciones móviles nativas deberían ser monolitos de implementación o si hubiera un equipo singular responsable del desarrollo de la interfaz.

Microservicios asincrónicos
Los microservicios síncronos realizan una solicitud a otros microservicios mientras procesa solicitudes y espera resultados. Los protocolos de comunicación asincrónica envían mensajes a los que los destinatarios reaccionan, pero no hay una respuesta directa. Un microservicio podría definirse como asíncrono si no realiza solicitudes a otros microservicios durante el procesamiento, o si realiza solicitudes, pero no espera los resultados.


![](https://res.cloudinary.com/practicaldev/image/fetch/s--Gx564mB7--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/69pkcy7lg0uj4960auq2.png)
Los microservicios asíncronos ofrecen varias ventajas notables a los microservicios síncronos y resuelven muchos de los desafíos de los sistemas distribuidos. La lógica requerida para manejar las solicitudes de microservicio no depende de los resultados, lo que los hace mucho más independientes.

Del mismo modo, si un socio de comunicación fallara, no se bloquea todo el sistema, ofreciendo resistencia general a su sistema. Además de eso, el procesamiento y la entrega casi siempre están garantizados.

Algunos ejemplos comunes de tecnologías para microservicios asíncronos son Kafka (una MOM comúnmente utilizada para mensajería), REST y formato de datos Atom (para infraestructura adicional).

Plataformas de microservicios
Las plataformas de microservicios, como PaaS y Docker Scheduler, admiten el funcionamiento y la comunicación de sus microservicios. Estas tecnologías permiten la comunicación entre microservicios para implementación, análisis de registros y monitoreo.

Por ejemplo, estas plataformas admiten HTTP y REST con equilibrio de carga y descubrimiento de servicios. Se necesita un soporte de operaciones limitado para la implementación de microservicios, de modo que puedan implementarse rápidamente y admitir múltiples microservicios.

Texto alternativo

Las plataformas de microservicios representan una simplificación y solución a problemas comunes. Algunas plataformas notables son Kubernetes y Docker, que es muy importante para las operaciones de microservicios. PaaS y Cloud Foundry también son útiles, pero no son tan populares.

Es importante tener en cuenta que la migración a estas plataformas requiere un cambio en la operación e instalación de aplicaciones, lo que puede hacer que el uso de una plataforma de microservicios sea un paso importante y oportuno. Este es el principal inconveniente de las plataformas de microservicios.

Terminando
Ahora que tiene una idea de lo que la arquitectura de microservicios tiene para ofrecer y qué variaciones hay, está listo para comenzar con un aprendizaje práctico. Eche un vistazo a nuestra lista de recursos a continuación para obtener más información sobre microservicios.

Recursos
Guía de microservicios: una colección de artículos aborda una variedad de temas relacionados con microservicios

El arte del monitoreo en la era de los microservicios: preguntas y respuestas útiles con el autor de "El arte del monitoreo" que cubre las estrategias de monitoreo

Building Microservices: el libro de O'Reilly sobre microservicios

Guía para principiantes de GitHub para microservicios: repositorio de código fácil de navegar para principiantes

Introducción a los microservicios de AWS: documentación de Amazon y definición de conceptos de microservicios

Arquitectura de microservicios: los cursos en línea definitivos
¿Busca un curso en línea en el que realmente pueda confiar? Lo cubrimos con una serie de microservicios de dos partes, todo lo que necesita saber, escrita por uno de los expertos en el campo, Eberhard Wolff, miembro fundador de la comunidad de Campeones de Java.

Comience con los principios básicos de los microservicios para obtener todas las bases necesarias para la implementación y la implementación.

Una Introducción a los Principios y Conceptos de Microservicio lo guía a través de todos los pros y los contras de esta emocionante tendencia utilizando ejemplos del mundo real y estrategias de migración.

Luego, puede pasar a la Arquitectura de microservicios: Implementación práctica, uno de los mejores cursos para los detalles esenciales de la implementación en el mundo real.
