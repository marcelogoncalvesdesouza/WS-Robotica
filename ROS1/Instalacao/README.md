[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)

Para a instalação correta deve-se utilizar a versão abaixo da distro Ubuntu. Recomenda-se criar uma máquina virtual para a utilização do framework (última versão, descontinuada, não recebe mais suporte, atualizações ou correções).

## ISO do Ubuntu 20.04 (Focal Fossa) LTS
```
https://releases.ubuntu.com/focal/ubuntu-20.04.6-desktop-amd64.iso
```

## Instalação do ROS 1 - Noetic
```
https://wiki.ros.org/noetic/Installation/Ubuntu
```

### COMANDOS

- Passo 01: configuração da lista de recursos
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
- Passo 02: Instalar o curl (ferramenta de transferência de dados)
```
sudo apt install curl
```
- Passo 03: adicionar chaves
```
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
- Passo 04: atualizar o índice de pacotes Debian
```
sudo apt update
```
- Passo 05: instalação da versão desktop full (Tudo incluído no Desktop, além de simuladores 2D/3D e pacotes de percepção 2D/3D).
```
sudo apt install ros-noetic-desktop-full
```
- Passo 06: executar este script para todos os terminais bash usar o ROS.
```
source /opt/ros/noetic/setup.bash
```
- Passo 07: teste de execução do ROS 1
```
roscore
```
- Passo 08: editar o bashrc
```
sudo gedit ~/.bashrc
```
Adicionar no final do arquivo:
```
source /opt/ros/noetic/setup.bash
```
Obs.: caso instalar outra versão do ROS 1 ou o Ros 2 comentar esta linha para não haver conflito.
- Passo 09: teste final em três terminais
```
roscore
```
```
rosrun roscpp_tutorials talker
```
```
rosrun roscpp_tutorials listener
```

### Segundo teste

Obs.: ativando o Turtlesim

- Passo 01: roscore
- Passo 02: rosrun turtlesim turtlesim_node

### Criando uma workspace

- mkdir catkin_ws -> cd catkin_ws
- mkdir src (pacotes da ws) -> cd src
- catkin_init_workspace -> ls -> cd .. -> ls
- catkin_make (compilar o ws)
- ls (build, devel e src)
- source devel/setup.bash (o sistema reconhece a ws)

### Conceitos do ROS

- O ROS é uma rede de processamento peer-to-peer
- Conceitos básicos
Master - nodo principal que gerencia a rede
Nodo - processo de execução
Serviço de parâmetros distribuídos - acessíveis por todos os nodos
Serviços - comunicação direta entre dois processos
Tópicos - comunicação multicast entre vários processos
Bags - sistema de log de mensagens

## Master (roscore)

- Elemento central do ROS
- Responsável pelo registro de nodos, tópicos, serviços e parâmetros da rede
- A principal tarefa é permitir que os nodos se localizem
- Garante uma comunicação direta (peer-to-peer) entre os nodos

## Nodo
### (rosnode [cleanup, info, kill, list, machine, ping])

- Processos em execução
- Um sistema de controle de um robô geralmente utiliza vários nodos
- Por exemplo um nodo é responsável pelo controle da câmera e outro nodo é responsãvel por reconhecer objetos
- Um nodo é implementado utilizando as bibliotecas cliente do ROS como roscpp (C++) ou rospy (Python)

## Serviços: parâmetros distribuídos
### (rosparam [delete, dump, get, list, load, set])

- Dicionário multivariado compartilhado entre todos os nodos
- Os nodos podem acessar e modificar as variáveis em tempo de execução utilizando a ROS API
- Os parâmetros são definidos por uma dupla (nome, valor)

<b>EXEMPLO</b>
- roscore
- rosrun turtlesim turtlesim_node
- rosparam list
- rosparam get /turtlesim/background_b
- rosparam set /turtlesim/background_b 0
- rosparam get /turtlesim/background_b
- rosservice call /reset

## Serviços: comunicação direta entre dois processos
### (rosservice [args, call, find, info, list, type, url])

- Utiliza o paradigma requisição/resposta para trocar informações
- É uma comunicação entre dois nodos
- Comunicação bloqueante, o nodo que faz a requisição aguarda a resposta

<b>EXEMPLO</b>
- roscore
- rosrun turtlesim turtlesim_node
- rosservice call /spawn
- rosservice call /reset

# Tópicos: comunicação multicast entre vários processos
### (topic [bw, echo, find, hz, info, list, pub, type])

- Funciona como um barramento, onde os nodos trocam informações
- Utiliza a semântica Anuncia/Pública/Se escreve (Advertise/Publish/Subscribe)
- Mensagens fortemente tipadas conforme arquivos de descrição de mensagem do ROS
- Comunicação não bloqueante
- Pode haver múltiplos nodes publicando e se inscrevendo em um tópico

<b>EXEMPLO</b>
- roscore
- rosrun turtlesim turtlesim_node
- rosrun turtlesim turtle_teleop_key
- rostopic pub /turtle1/cmd_vel geometry_msgs/Twist tab ...
- rostopic pub -r 1 /turtle1/cmd_vel geometry_msgs/Twist tab ...
- rosrun rqt_graph rqy_graph
- rosmsg show geometry_msgd/Twist

