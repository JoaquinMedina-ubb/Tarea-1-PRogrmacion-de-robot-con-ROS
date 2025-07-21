# Tarea-1-PRogrmacion-de-robot-con-ROS

Explicación de los modelos para correr en gazebo

# Three DOF Robot - ROS 2 & Gazebo Simulation

Este paquete define y simula un robot de 3 grados de libertad (3DOF) utilizando ROS 2 y Gazebo (Ignition). Incluye la descripción del robot, configuraciones para `ros2_control`, y scripts de lanzamiento para visualizar y simular el robot en un entorno virtual.

---

## Contenido del Proyecto

### 1 Descripción del Robot
- **robot_3dof.xacro**  
  Define la estructura física del robot (links, joints) en formato Xacro, incluyendo geometría, materiales e inercia.

- **three_dof.gazebo.xacro**  
  Añade configuraciones específicas para la simulación en Gazebo, como plugins de `gazebo_ros2_control`.

- **three_dof.ros2control.xacro**  
  Configura los controladores de ROS 2 Control (posición y estados de las articulaciones).

---

### 2️Scripts de Lanzamiento
- **rsp.launch.py**  
  Procesa el archivo Xacro, genera el URDF y lanza `robot_state_publisher` para publicar la descripción del robot.

- **three_dof_sim.launch.py**  
  Orquesta la simulación completa:
  1. Carga la descripción del robot.
  2. Lanza Gazebo con un entorno vacío.
  3. Publica el modelo en `/robot_description`.
  4. Configura el puente ROS 2 ↔ Ignition.
  5. Inicia los controladores:
     - `joint_state_broadcaster`
     - `joint_trajectory_controller`

---

##  Requisitos

- **ROS 2** (Humble o Jazzy)
- **Ignition Gazebo** (`ros_gz_sim` y `ros_gz_bridge`)
- **ros2_control** y **controller_manager**
- **xacro**
- Python 3.8+
