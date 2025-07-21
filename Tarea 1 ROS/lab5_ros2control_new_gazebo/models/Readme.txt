# Three DOF Robot Description

Este paquete contiene la descripción del modelo de un robot de 3 grados de libertad (3DOF) para ROS2, incluyendo sus archivos Xacro y configuraciones para simulación en Gazebo.

## Archivos

- **robot_3dof.xacro** 
  Define la estructura del robot, incluyendo sus links y joints. Este archivo es el principal para generar el URDF.

- **three_dof.gazebo.xacro** 
  Añade configuraciones específicas para la simulación en Gazebo, como plugins y parámetros físicos.

- **three_dof.ros2control.xacro** 
  Configura los controladores ROS2 Control para gestionar los movimientos de los joints durante la simulación.

