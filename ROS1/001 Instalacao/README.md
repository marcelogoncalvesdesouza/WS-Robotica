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

### Comandos

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

- Passo 10: segundo teste em dois terminais - ativando o Turtlesim

```
roscore
```
```
rosrun turtlesim turtlesim_node
```
[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)