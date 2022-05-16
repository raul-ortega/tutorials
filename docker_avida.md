# Ejecutar avida en un contenedor de Docker

## Instalar Docker en ubuntu 20.04

- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-es

## Instalar Docker en Windows 10

- https://www.youtube.com/watch?v=9awV3Y-rpI0


## avida pre-compilado en una imagen existente

Descargar imagen

```
sudo docker pull raulya/avida:2.15
```

Comprobar que se ha descargado:

```
sudo docker images
```

![](img/docker_avida_1.png)

Ejecutar el contenedor y abrir sesión

```
docker ru -it raulya/avida:2.15 /bin/bash
```

Ejecutar avida

```
cd avida/
./avida -version
```

El resultado debe ser:

    ```
    Avida 2.15.0
    --------------------------------------------------------------------------------
    by Charles Ofria
    Lead Developer: David M. Bryson

    Active developers include:
    Aaron P. Wagner and Anya E. Johnson
    For a more complete list of contributors, see the AUTHORS file.

    Copyright 1999-2014 Michigan State University.
    Copyright 1993-2003 California Institute of Technology.

    Avida comes with ABSOLUTELY NO WARRANTY.
    This is free software, and you are welcome to redistribute it under certain
    conditions. See file COPYING for details.

    For more information, see: http://avida.devosoft.org/
    --------------------------------------------------------------------------------
    ```

