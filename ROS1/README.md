[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main)

# ROS 1 (Robot Operating System 1)

Site oficial
```
https://www.ros.org/
```

- O simulador do ROS 1 (Robot Operating System) funciona como um ambiente virtual que permite testar e desenvolver código para robôs sem precisar do hardware físico. Ele atua criando uma "cópia digital" do robô e do mundo real, processando comandos e retornando dados de sensores exatamente como um robô de verdade.
- O ecossistema de simulação do ROS 1 é composto principalmente por duas ferramentas que trabalham juntas:

# O Simulador Físico: Gazebo
É o simulador principal. Ele simula a física do mundo real. 

## O que faz:
- Calcula gravidade, colisões, atrito e massa.
- Sensores: Simula o que o robô "vê" ou "sente", como câmeras, scanners a laser (LiDAR), sensores ultrassônicos e GPS.
- Atuadores: Simula motores, rodas, braços robóticos e articulações

# A Ferramenta de Visualização: RViz

O RViz é a interface gráfica de monitoramento. 

## O que faz:
- Permite visualizar o que o robô está "pensando" e percebendo.
- Visualização - Mostra o modelo 3D do robô, mapas gerados pelo ambiente, rotas de navegação planejadas e nuvens de pontos.

[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main)