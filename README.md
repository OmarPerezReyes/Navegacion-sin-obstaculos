# Navegacion sin obstáculos
Código en C++ sobre la prueba correspondiente del proyecto dotMex_Car del Laboratorio de Robótica y Visión Artificial del Cinvestav Zacatenco, creado originalmente en lenguaje Python utilizado en el Torneo Mexicano de Robótica 2022 para la categoria AutoModelCar.

## Requerimientos:
* Ubuntu 18.04
* ROS Melodic
* Webots 2021b: https://github.com/cyberbotics/webots/releases

## Instalación:
Nota: se asume que ya se tiene instalado Ubuntu y ROS.
* Seguir las instrucciones para instalar Webots: https://cyberbotics.com/doc/guide/installing-webots
* $ git clone https://github.com/OmarPerezReyes/Navegacion-sin-obstaculos.git
* $ cd Navegacion-sin-obstaculos
* $ cd catkin_ws
* $ catkin_make
* $ source devel/setup.bash

## Ejecución
Después de correr el .launch correspondiente a la prueba a partir de la documentación proporcionada en el repositorio: https://github.com/mnegretev/TMR-2022-AutoModelCar
* $ rosrun nav_no_obstacles nav_no_obstacles
