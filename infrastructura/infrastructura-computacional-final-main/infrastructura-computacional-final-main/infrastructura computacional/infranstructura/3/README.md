1 se crearon los dos grupos desde mi usuario con el comando:
sudo groupadd profesores sudo groupadd estudiantes

![163656362-5f2c5016-c245-4488-b974-5bbeaff77991](https://user-images.githubusercontent.com/101077186/169584381-57124529-3395-4cca-99b7-7838bf531581.png)

2  se crearon los tres respectivos usuarios con el comando sudo adduser

![Screenshot from 2022-05-16 01-23-49](https://user-images.githubusercontent.com/101077186/169584543-a1bda808-ca39-47de-83cd-01c3b60991d2.png)


3 Se asignaron los usuarios a los grupos de la siguiente forma :
grupo profesores — diana y Claudia
 grupo estudiantes — laura
el comando que se uso es sudo usermod usuario creado –G grupo 

![163656362-5f2c5016-c245-4488-b974-5bbeaff77991](https://user-images.githubusercontent.com/101077186/169584590-5618a9e5-bc1e-4468-8e61-6566c2273a58.png)

4 Se crearon los directorios D.Profes y D.Estudiantes con el comando mkdir en la ubicación /home esto para evitar los problemas con los permisos de cada usuario

5  les asigno el respectivo grupo dueño a los directorios recientemente creados con el comando:
sudo chgrp -R profes /home/D.Profesores — El grupo profesores es dueño del directorio D.Profesores
sudo chgrp -R estudiantes /home/D.Estudiantes — El grupo estudiantes es dueño del directorio D.Estudiantes

![Screenshot from 2022-05-16 01-32-17](https://user-images.githubusercontent.com/101077186/169584856-b3c4ddd4-0167-4e08-8a62-a9291e11988d.png)

6 Se les asigno los respctivos accesos como lo indica el punto con el comando:
sudo chmod 070 /home/D.Profes — Da acceco de rwx a grupos
sudo chmod 077 /home/D.Estudiantes — Da acceco de rwx a grupos y otros

7 Se verificaron los permisos anteriormente concedidos entrando a cada usuario con el comando : sudo su nombreUsuario y viendo si este tenia acceso a su o sus respectivos directorios
![Screenshot from 2022-05-16 01-39-39](https://user-images.githubusercontent.com/101077186/169585301-04bd245a-d669-4106-a933-4fa408f3e4ad.png)

8  Entre a los directorios creados con los tres usuarios y con cada uno cree un archivo con el comando vi

9  Cambie el usuario a súper usuario (root) y revise el dueño de los directorios , el resultado es el siguiente

10 Después intercambie de dueños a los archivos notasPrimerCorte y notasSegundoCorte con el comando:

chown claudia notasPrimerCorte
chown diana notasSegundoCorte
Quedaría de la siguiente manera:

11 Usando diferentes terminales accedí al sistema equivocándome algunas veces en el nombre de usuario o contraseña dedspues de hacer esto da como una clase de cooldawn para volverlo a hacer

12  con el comando last liste los ingresos al sistema y pude ver que laura ingreso varias  veces al sistema

13 por ultimo con el comando con el comando tar cvfz comprimi el directorio D.Profes en un archivo .tgz con el nombre profes.tgz e hice lo mismo con el de los estudiantes 
