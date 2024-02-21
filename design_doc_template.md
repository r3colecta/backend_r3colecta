# Titulo: Documento de Diseño R3colecta
---
## Overview: Problema a resolver
R3colecta es un Organización sin Fines de Lucro que promueve practicas y actividades sostenibles, para beneficio del medio ambiente, por medio proyectos de Reciclaje, Arborización y Generación de Energías Alternativas, para este fin la Organización busca compromoter a la comunidad en este tipo de actividades para lo cual se ha propuesto el desarrollo de una aplicación movil que permita, recompensar a las personas por realizar actividades de catpura de CO2 las mismas que pueden ser:
Caminar:  (como alternativa al uso de Movilidad reduciéndo así la cantidad de CO2 emitido al medio ambiente) dentro de la aplicación se denominará como Plooging (actividad que consiste en caminatas en las cuales se realiza recoleción de residuos)

Reciclar: Esta actividad consiste en el proceso de reciclaje de residuos en el hogar haciendo uso de de un scanner de codigo QR

Acopiar: esta actividad consiste en el registro de residuos en puntos de acopio. (Solo para emprendimientos)

Arborización: esta activiadad consiste en el registro de puntos de arborización (Solo para Personal de R3colecta)

Cada una de estas actividades (a excepción de la de Arborización) debe generar un sistema de puntos que permita a los usuarios intercambiar por servicios, productos o activos digitales (Criptomonedas, NFTs, otros)

### Alcance(Scope)
Diseño de APP mobile, desarrollo del backend, desarrollo de la base de datos NoSQL

#### Casos de uso
Descripción...
* Caso de uso 1: El usuario debe registrarse en la aplicación por media de su cuenta de google o Facebook
* Caso de uso 2: El usuario debe elegir la opción segun el perfil creado en base a la actividad (Acopiar, Reciclar, Caminar)
* Caso de uso 3: Una vez elegido el Perfil se debe mostrar la interface que corresponda, midiendo en cualquiera de ellas la cantidad de CO2eq Recuperado
* Caso de uso 4: El usuario con Perfil "Caminar" debe acceder a la funcionalidad del contador de pasos integrado al celular para realizar el calculo correspondiente
* Caso de uso 5: El usuario con Perfil "Acopiar" debe acceder a la funcionalidad del llenado de formulario, en base a los adjuntos de la funcionalidad Acopiar
* Caso de uso 6: El usuario con Perfil "Reciclar" debe acceder a la funcionalidad del llenado de formulario, en base a los adjuntos de la funcionalidad Reciclar
* Caso de uso 7: El usuario con Perfil "Arborización" debe acceder a la funcionalidad del llenado de formulario, en base a los adjuntos de la funcionalidad Arborización restringido solo para usuarios de la Organización
* Caso de uso 8: Todos los perfiles (a excepcion del de arborización) deben contar con la opción de "Estadisticas" para poder ver el avance de sus actividades, los mismos estaran representados por CO2eq recuperado por dia
* Caso de uso 9: Todos los perfiles (a excepcion del de arborización) deben tener acceso a las opciones: "Recompensas", "Comunidades", "Canjear Activos Digitales"
* Caso de uso 10: "Recompensas", Permite visualizar una lista de Empresar o Servicios mediantes los cuales los usuarios pueden canjear sus puntos
* Caso de uso 11: "Comunidades", Permite visualizar una lista de Comunidades mediante la cual se pueden realizar activiades de forma conjunta.
* Caso de uso 12: "Activos Digitales" Permite a los usuario intercambiar sus puntos por Activos Digital "Criptomonedas" o "NFTs"
* Caso de uso 13: "Transferencias" Permite a los usuario enviar y recibir los puntos ganados
* 
* ...

#### Out of Scope (casos de uso No Soportados)
Descripción...
* Caso de uso 1
* Caso de uso 2
* ...
---
## Arquitectura

ENTORNO 1: BASE DE DATOS (MONGODB) (CLOUD)
ENTORNO 2: CACHE/BASE DE DATOS (REDIS)
ENTORNO 3: BACKEND (NEST.JS) (VERCEL)
ENTORNO 4: FRONTEND (RECT NATIVE)


(ENTORNO 4) APPMOVIL----------------BACKEND (ENTORNO 3)
                                      |-------------(POST)---------- (ENTORNO 1)
                                      |-------------(GET)----------- (ENTORNO 2)
                                      |-------------(PATCH)--------- (ENTORNO 1)
                                      |-------------(DELETE)---------(ENTORNO 1)


### Diagramas
poner diagramas de secuencia, uml, etc (a definir)

### Modelo de datos
Poner diseño de entidades, Jsons, tablas, diagramas entidad relación, etc.. (a definir)

---
## Limitaciones
Lista de limitaciones conocidas. Puede ser en formato de lista.
Ej.
* Llamadas del API tienen latencia X
* No se soporta mas de X llamadas por segundo
---
## Costo
Descripción/Análisis de costos
Ejemplo:
"Considerando N usuarios diarios, M llamadas a X servicio/baseDatos/etc"
* 1000 llamadas diarias a serverless functions. $XX.XX
* 1000 read/write units diarias a X Database on-demand. $XX.XX
Total: $xx.xx (al mes/dia/año)
