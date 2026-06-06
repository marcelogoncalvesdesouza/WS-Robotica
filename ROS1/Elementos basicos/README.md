[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)

- <b>Nós (<i>nodes</i>)</b>: executáveis, processos, códigos que realizam alguma atividade, não necessariamente no mesmo sistema
- <b>Tópicos (<i>topics</i>)</b>: forma de troca de informações (mensagens) entre os nós
- <b>Serviços (<i>services</i>)</b>: interação entre nós de forma a solicitar uma ação ou dado com uma resposta, arquivos de descrição de serviços
- <b>Pacotes (<i>packages</i>)</b>: unidade principal de organização do ROS, arquivos e códigos

- <b>Metapacotes (<i>metapackages</i>)</b>: pacotes especializados que servem para representar um grupo de pacotes
- <b>Package Manifest</b>: são arquivos xml com informações osbre um pacote
- <b>Repositórios</b>: coleção de pacotes compartilhados
- <b>Mensagens</b>: arquivos de descrição de mensagem
- <b>Launchs</b>: arquivos xml que especificam a execução de um sistema e seus parâmetros

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

[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)