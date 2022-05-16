1. Descargar e **Instalar Virtual Box**

    - https://www.virtualbox.org

    ![](img/virualbox_docker_0.png)

1. **Ejecutar Virtual Box**
    
1. Menú Máquina > **Nueva** (o bien CTRL + D)

   ![](img/virualbox_docker_1.png)

1. Nombre: ubuntu-20.04

   - Tipo: **Linux**
   - Versión: **Ubuntu (64-bit)**
   - Tamaño de memoria: **4098** (requisito de Docker)
   - Crear un disco virtual ahora: Seleccionado

   ![https://www.virtualbox.org](img/virualbox_docker_2.png)
   
   Click en botón **Crear**
   
   ![](img/virualbox_docker_3.png)
   
   Click en botón **Crear**
   
   
1. **Descargar** imagen **Ubuntu Desktop 20.04**

   - https://ubuntu.com/download/desktop
   
   ![](img/virualbox_docker_5.png)

   
1. VirtuaBox
   Configuración > Almacenamiento > Controlador IDE > Vacio >
   **Seleccione Archivo de Disco Virtual**
   
   ![](img/virualbox_docker_6.png)
   
   **Marcar CD/DVD Vivo (Live)**
   
   ![](img/virualbox_docker_8.png)
   
   
1. **Iniciar** Máquina Virtual (**Inicio desacoplado**).

   ![](img/virualbox_docker_9.png)

1. **Instalar Ubuntu** (Install Ubuntu)

   ![](img/virualbox_docker_10.png)

   - Selecciona Idioma y Teclado
   - Erase disk > Intall Now > Continue
   - Zona Horaria
   - Nombre de usuario, máquina y contraseña
   
   ![](img/virualbox_docker_11.png)
   
   ![](img/virualbox_docker_12.png)
   
   Esperamos unos minutos hasta finalizar la instalación
      
   ![](img/virualbox_docker_13.png)
   
   **Reiniciar** (Restart Now)
   
   ![](img/virualbox_docker_14.png)
   
1. VirtualBox > Configuración > **Eliminar Disco Virtual**

   ![](img/virualbox_docker_15.png)
   
   Presionar **Enter**
   
1. Cambiar **Resolución de Pantalla**

   Click botón derecho sobre el escritorio
   
   Settings > Display > Resolution
   
   Elegir resolución deseada (ejemplo 1280 x 800).
   
   ![](img/virualbox_docker_16.png)
   
   Clic en **Apply** (Aplicar)

1. Abrimos una **terminal** (CTRL + T)


   ![](img/virualbox_docker_17.png)
   
   
1. **Instalar herramientas**

    Actualizar fuentes

    ```
    sudo apt-get update
    ```
    
    Instalar paquetes
    
    ```
    sudo apt-get -y install ca-certificates gcc-9 g++-9 make=4.2.1-1.2 cmake=3.16.3-1ubuntu1  git=1:2.25.1-1ubuntu3.4 curl
    ```
    
1.  Clonar repositorio avida

    Crear directorio
    
    ```
    mkdir /home/mi_usuario/github
    ```

    Saltar al directorio
    
    ```
    cd /home/mi_usuario/github
    ```
    
    Clonar avida
    
    ```
    git clone https://github.com/fortunalab/avida.git
    ```
    
    ![](img/virualbox_docker_18.png)
    
    Saltar a directorio avida
    
    ```
    cd avida/
    ```
    
    Actualizar submódulos
    
    ```
    git submodule update --init --recursive
    ```
    
    ![](img/virualbox_docker_19.png)
    
1.  **Compilar avida**

    Compilamos avida ejecutando el script build-avida
    
    ```
    ./build_avida
    ```
    
    El comando anterior puede dar un error debido a que usa 10 hilos para la compilación.
    Para solucionarlo podemos ejecutar los siguientes comandos
    
    ```
    cd /home/ubuntu/github/avida
    rm -R cbuild/
    mkdir -p cbuild
    cd cbuild
    cmake ../
    make
    make install
    ```
    
    
1.  **Ejecutar avida**

    Los archivos finales son creados en cbuild/work/bin
    
    ```
    cd work
    ```
    
    Listamos archivos
    
    ```
    ls -l
    ```
    
    ![](img/virualbox_docker_20.png)
    
    
    Comprobamos número de versión
    
    ```
    ./avida -version
    ```    
    
    ![](img/virualbox_docker_21.png)
    
