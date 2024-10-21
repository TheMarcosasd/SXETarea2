Entregar el repositorio

Utilizaremos la imagen de Alpine. Sigue las instrucciones:
    1 Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo
    2 Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre
    3 Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?
    4 Comprueba que ip tiene y si puedes hacer un ping a google.com
    5 Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?
    6 Sal del terminal, ¿que ocurrió con el contenedor?
    7 ¿Cuanta memoria en el disco duro ocupaste?
    8 ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

Llendo a la pagina oficial de docker, buscamos alpine y en su pagina nos muestra el comando "docker pull alpine"

![Screenshot_20241017_123019](https://github.com/user-attachments/assets/ee78661d-137f-45ff-a669-bc937fb05388)

Comprobacion de que se realizo el comando

![Screenshot_20241017_122808](https://github.com/user-attachments/assets/8de800ff-56f5-40e1-987b-b28779c5c488)

Y comprobacion de que lo descargado es en realidad sorprendentemente una imagen

![Screenshot_20241017_123935](https://github.com/user-attachments/assets/cf46bade-946e-42b2-935a-3987a5ee906b)

Ahora tenemos que crear un contenedor sin nombre, para ello usamos docker create con el nombre de la imagen a usar. 
Sin el nombre de la imagen no nos dejara hacerlo

![Screenshot_20241017_125903](https://github.com/user-attachments/assets/fe7ecf79-dc23-4af4-a119-e2820d654e7b)

Al ser creado no se arranca automaticamente, lo sabremos al usar el comando "docker ps". El cual nos lista los contenedores
"activos", sin embargo añadiendole "-a" nos muestra tambien los "parados"

![Screenshot_20241017_125934](https://github.com/user-attachments/assets/9a79ee59-0553-49f2-92d4-75e30c720d20)

El nombre dado al contenedor creado es condescescending_goldstine

Ahora tenemos que crear un contenedor llamado dam_alp1 con la imagen alpine

![Screenshot_20241021_101858](https://github.com/user-attachments/assets/bd2673d0-9bf6-4062-81e8-0455fba53cd6)

Y accedemos al contenedor

![Screenshot_20241021_105432](https://github.com/user-attachments/assets/e79ac9a6-5ac8-4507-acc4-d5872bc4aa2c)

Comprobamos la ip 

![Screenshot_20241021_131625](https://github.com/user-attachments/assets/e853c52f-f30c-4c1a-a7ab-1d44c480113b)

Le hacemos ping a google

![Screenshot_20241021_132008](https://github.com/user-attachments/assets/fe7f716d-8d1e-459e-bc8b-6bdb0b747da4)

Creamos el contenedor dam_alp2 y le hacemos ping a dam_alp1

![Screenshot_20241021_132532](https://github.com/user-attachments/assets/97fdc84d-57fc-4382-98bc-f66471ff2884)

Tras salir de la temerinal los contenedores siguieron activos independientemente de la terminal

![Screenshot_20241021_135453](https://github.com/user-attachments/assets/e2d8208c-d1de-4298-9904-c58e4e756f74)

A continuacion comprobamos cuanta memoria se ha ocupado

![Screenshot_20241021_135632](https://github.com/user-attachments/assets/c8c4157e-d5c9-4df1-a052-8f4dad643fb4)

Por ultimo vemos la ram usada (sin querer pare los contenedores)
comando usado docker stats

![Screenshot_20241021_140300](https://github.com/user-attachments/assets/b6a82400-f98a-460f-9ebc-7e372ddd5900)
