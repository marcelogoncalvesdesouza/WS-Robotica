[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)

## Criando um ROS Package

- Acessar o catkin_ws e digitar
```
source devel/setup.bash
```
- Acessar o src
```
catkin_create_pkg meu_pacote roscpp rospy std_msgs
```
- package.xml: Arquivo de manifesto do pacote;
- CMakeLists: Informações dos códigos que precisarão serem compilados.

Compilar novamente o ws:
```
catkin_make
```
Confirmar a compilação do ws
```
source devel/setup.bash
```
```
roscd meu_pacote
```