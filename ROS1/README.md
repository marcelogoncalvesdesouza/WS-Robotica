[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main)

# ROS 1 (<i>Robot Operating System 1</i>)

## Características

- Framework para desenvolvimento de software para robótica
- Open source
- Grande modularidade e compartilhamento
- Comunidade ativa

## Site oficial
```
https://www.ros.org/
```

- [Instalação](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1/Instalacao)
- O simulador do <b>ROS 1</b> (<i>Robot Operating System</i>) funciona como um ambiente virtual que permite testar e desenvolver código para robôs sem precisar do hardware físico. Ele atua criando uma "cópia digital" do robô e do mundo real, processando comandos e retornando dados de sensores exatamente como um robô de verdade.
- O ecossistema de simulação do ROS 1 é composto principalmente por duas ferramentas que trabalham juntas:

## O Simulador Físico: Gazebo
- É o simulador principal. Ele simula a física do mundo real. 

## O que faz:
- <b>Cálculos</b>: Calcula gravidade, colisões, atrito e massa.
- <b>Sensores</b>: Simula o que o robô "vê" ou "sente", como câmeras, scanners a laser (LiDAR), sensores ultrassônicos e GPS.
- <b>Atuadores</b>: Simula motores, rodas, braços robóticos e articulações

## A Ferramenta de Visualização: RViz
- O RViz é a interface gráfica de monitoramento. 

## O que faz:
- <b>Visualização</b>: Permite visualizar o que o robô está "pensando" e percebendo e mostra o modelo 3D do robô, mapas gerados pelo ambiente, rotas de navegação planejadas e nuvens de pontos.

## Elementos básicos
- <b>Nós (<i>nodes</i>)</b>: executáveis, processos, códigos que realizam alguma atividade, não necessariamente no mesmo sistema
- <b>Pacotes (<i>packages</i>)</b>: unidade principal de organização do ROS, arquivos e códigos
- <b>Metapacotes (<i>metapackages</i>)</b>: pacotes especializados que servem para representar um grupo de pacotes
- <b>Package Manifest</b>: são arquivos xml com informações osbre um pacote
- <b>Repositórios</b>: coleção de pacotes compartilhados
- <b>Mensagens</b>: arquivos de descrição de mensagem
- <b>Serviços (<i>services</i>)</b>: interação entre nós de forma a solicitar uma ação ou dado com uma resposta, arquivos de descrição de serviços
- <b>Launchs</b>: arquivos xml que especificam a execução de um sistema e seus parâmetros
- <b>Tópicos (<i>topics</i>)</b>: forma de troca de informações (mensagens) entre os nós

## Espaço de trabalho (catkin_ws)
- Pacotes: um package é como uma aplicação ROS é feita
- Cada pacote pode possuir uma ou mais aplicações que utiliza uma ou mais de uma linguagem
- A workspace é onde ficam os packages

## Estrutura de um WS
- build: arquivos compilados
- devel: variáveis de ambiente
- src: pacotes e aplicações

## Exemplo 01
- Motores com enconders (C++)
- Raspberry Pi (C++)
- Câmera (Python)

## Links
- ROS Wiki
```
https://wiki.ros.org
```
- ROS Tutorials
```
https://wiki.ros.org/ROS/tutorials
```
- ROS Answer
```
https://answers.ros.org
```
- ROS Discourse
```
https://discourse.ros.org
```

[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main)