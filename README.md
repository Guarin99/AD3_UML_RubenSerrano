# AD3_UML_RubenSerrano

##Autor
Ruben Serrano Nohales
Guarin99

 

##1. Análisis del problema y requisitos del sistema

• ¿Quiénes son los actores que interactúan con el sistema?

En este supuesto tendriamos solo la figura del administrador como actor.

• ¿Cuáles son las acciones que cada actor puede realizar?

Nuestro actor tiene unas acciones definidas en el diagrama de casos de uso, que son:

*Registrar Equipo <include> Comprobar Existencia de Equipo.
*Añadir Jugadores a un Equipo <include> Comprobar Existencia de Equipo.
                              <include>Comprobar si el Jugador esta Inscrito <include> Consultar la Lista de Equipos.
                                                                             <include> Mostrar Numero de Jugadores por Equipo.
*Consultar la Lista de Jugadores <include>  Consultar la Lista de Equipos 
                                 <include> Mostrar Numero de Jugadores por Equipo.
                                 
• ¿Cómo se relacionan entre sí las entidades del sistema?
Las entidades son:
Equipo
Jugador

Un Equipo tiene muchos Jugadores y un Jugador tiene solo un equipo.
Con esto traducimos la cardinalidad de uno a muchos

EQUIPO --------------->Jugador 
      1               *
      
El este caso de uso, yo he definino la relacion como una composicion, quiero que todos los jugadores tengan un equipo, que no sea posible que 
un jugador exista sin equipo asignado.





##2. Identificación de los casos de uso y elaboración del diagrama

Actor:
Administrador

Casos de uso:
Registrar equipo -<include>->Comprobar Existencia De Equipo.
Añadir jugadores a un equipo-<include>->Comprobar Existencia De Equipo.
                            -<include>->Comprobar si el Jugador Esta Inscrito.
                            -<include>->Mostrar Numero de jugadores por equipo.
Consultar lista de equipos y jugadores-<include>->Consultar la Lista de Equipos.
                                      -<include>->Mostrar el Numero de Jugadores por Equipo.

##3. Identificación de clases y relaciones

Clases:
Equipo
Jugador

Clase de control:
Sistema Gestor


Relacines:
Equipo----Composicion--->Jugador
             1..*

SistemaGestor---Asociacion--->Equipo



##Explicacion del diseño

Mi interpretacion de este supuesto identifica a un actor como administrador de nustro sistema con los tres casos de uso que nos dice el enunciado,
Registrar equipo, Añadir jugador a un equipo y consultar la lista de equipos y jugadores.

En el caso de uso Registrar equipo he hecho un <include> hacia otro caso de uso Comprobar existencia de Equipo , interpreto que es un include porque quiero
que el caso de uso Registrar equipo siempre verifique que el equipo a registrar no esta ya registrado para evitar duplicidad.

Añadir jugadores tambien incluye este caso de uso Comprobar existencia de Equipo, siempre que se añada un jugador debo comprpbar que el equipo esta registrado,
y si no registarlo.
Tambien incluye otro caso de uso para comprobara si el jugador que se añade esta ya inscrito, no registarlo de nuevo, que a su vez incluye consultar la lista de equipos,
para comprobar si el jugador en cuestion estuviese en otro equipo ya registrado y otro caso de uso que seria mostrar numero de jugadores, para que todos los equipos tengan un 
minimo de jugadores y un maximo.

Consultar la lista de jugadores incluye el caso de uso consultar lista de equipos para poder identificar a que equipo pertenece cada jugador, 
incluyendo tambien el caso de uso Mostrar numero de jugadores por equipo, que nos daria como resultado el listado de jugadores con el equipo perteneciente 
y la cantidad jugadores por equipo.

Conclusion del aprendizaje

Considero que el UML es de una importancia vital, nos ayuda a ver las la logica del sofware no como usuarios, sino como actores y asi entender cuales seran las funciones 
y las necesidades de el proyecto a desarroyar.
No me ha resultado facil hacer el ejercicio de ver el sistema desde el punto de vista de un actor y identificar los metodos, al final buscando informacion y con las explicaciones de clase
pude hacer la entrega de esta actividad, otra cosa es el resultado.
Gracias Luis por tu atencion y esfuerzo.

