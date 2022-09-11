Como primer paso en nuestra maquina virtual entramos al Login en modo root asi:
    su -
   Luego colocamos su password.

Como segundo paso crearemos 3 usuarios de la siguiente manera.
   useradd: Dario
   useradd: Evelyn
   useradd: Kevin
Para Su verificacion de creacion usaremos el comando.
   cat /etc/passwd 

Tercer paso creamos un grupo llamado casa.
   -groupadd casa
   Para Su verificacion de creacion usaremos el comando.
   -cat /etc/grupo
   
Cuarto paso añadimos los usuarios al grupo casa.
  useradd: Dario
  useradd: Evelyn
  useradd: Kevin
Para Su verificacion de creacion usaremos el comando.
   cut -d: -f1,4 /etc/passwd 

Paso cinco Cambiamos de nombre al grupo casa por [Familia]
   groupmod -n Familia casa
  Para Su verificacion de creacion usaremos el comando.
   cat /etc/group
 
 Para eliminar dichos Grupo o nombres
   userdel -r Kevin         -Para eliminar usuario
   groupdel casa            -Para eliminar grupo
   deluser kevin Familia    -para eliminar usuario de un grupo
