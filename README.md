# Simuladores para Robótica

## [4DV-Sim](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/4DV-Sim)
- O 4DV-Sim (desenvolvido pela 4D Virtualiz e distribuído pela OPAL-RT) é um ambiente de simulação 3D em tempo real focado no desenvolvimento, teste e certificação de veículos autônomos, robôs e drones. Ele permite criar "gêmeos digitais" para testar algoritmos com segurança antes de aplicações no mundo real.

## [ROS 1](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)
- O simulador do ROS 1 (Robot Operating System) funciona como um ambiente virtual que permite testar e desenvolver código para robôs sem precisar do hardware físico. Ele atua criando uma "cópia digital" do robô e do mundo real, processando comandos e retornando dados de sensores exatamente como um robô de verdade.

## [ROS 2](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS2)
- A principal diferença é que o ROS 1 dependia de um servidor central ("Master") e foi projetado para pesquisa acadêmica. O ROS 2 utiliza uma arquitetura descentralizada com o protocolo industrial DDS e foco nativo em tempo real, segurança e ambientes comerciais.

## [V-REP](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/V-REP)
- O V-REP (atualmente renomeado para CoppeliaSim) é um poderoso software de simulação robótica 3D. Ele funciona criando um ambiente digital para projetar, programar e testar robôs e sistemas de automação antes de construí-los no mundo real.

## [Webots](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/Webots)
- Quando uma simulação é iniciada, o Webots executa os controladores especificados, cada um como um processo separado, e associa os processos dos controladores aos robôs simulados. Observe que vários robôs podem usar o mesmo código de controlador; no entanto, um processo distinto será executado para cada robô.

# LINKS

- Kobuki
```
https://robots.ros.org/kobuki/
```

ATUALIZAÇÃO DE REPOSITÓRIO
```
git add .
git commit -m "Update."
git push -u origin main
```
```
git pull origin main
```