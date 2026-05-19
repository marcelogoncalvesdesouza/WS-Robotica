## Simuladores

## ROS 1
- O simulador do ROS 1 (Robot Operating System) funciona como um ambiente virtual que permite testar e desenvolver código para robôs sem precisar do hardware físico. Ele atua criando uma "cópia digital" do robô e do mundo real, processando comandos e retornando dados de sensores exatamente como um robô de verdade.
- O ecossistema de simulação do ROS 1 é composto principalmente por duas ferramentas que trabalham juntas:
1. O Simulador Físico: Gazebo
O Gazebo é o simulador principal. Ele simula a física do mundo real. 

O que faz: Calcula gravidade, colisões, atrito e massa.
Sensores: Simula o que o robô "vê" ou "sente", como câmeras, scanners a laser (LiDAR), sensores ultrassônicos e GPS.
Atuadores: Simula motores, rodas, braços robóticos e articulações

2. A Ferramenta de Visualização: RViz

O RViz é a interface gráfica de monitoramento. 

O que faz - Permite visualizar o que o robô está "pensando" e percebendo.
Visualização - Mostra o modelo 3D do robô, mapas gerados pelo ambiente, rotas de navegação planejadas e nuvens de pontos.

## V-REP
- O V-REP (atualmente renomeado para CoppeliaSim) é um poderoso software de simulação robótica 3D. Ele funciona criando um ambiente digital para projetar, programar e testar robôs e sistemas de automação antes de construí-los no mundo real.
## Webots
- Quando uma simulação é iniciada, o Webots executa os controladores especificados, cada um como um processo separado, e associa os processos dos controladores aos robôs simulados. Observe que vários robôs podem usar o mesmo código de controlador; no entanto, um processo distinto será executado para cada robô.
## 4DV-Sim
-O 4DV-Sim (desenvolvido pela 4D Virtualiz e distribuído pela OPAL-RT) é um ambiente de simulação 3D em tempo real focado no desenvolvimento, teste e certificação de veículos autônomos, robôs e drones. Ele permite criar "gêmeos digitais" para testar algoritmos com segurança antes de aplicações no mundo real.

ATUALIZAÇÃO DE REPOSITÓRIO
```
git add .
git commit -m "Update."
git push -u origin main
```

