[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main)

# ROS 2 (<i>Robot Operating System 2</i>)

Ricardo Grando - FURG
Minicurso ROS2: https://www.youtube.com/watch?v=7T3lgJEQ8PE&list=PLhxZVyws6Ytssb_CJA5cKxY5IxecOvJao

## Características

### Arquitetura de Comunicação

- ROS 1: Utiliza o sistema Master-Slave. Se o nó central cair, toda a descoberta de novos dispositivos é interrompida.
- ROS 2: Totalmente descentralizado (Peer-to-Peer) usando o middleware DDS (Data Distribution Service). Não há ponto único de falha e os robôs se comunicam de forma autônoma e direta.

### Qualidade de Serviço (QoS)

- ROS 1: Comunicação rígida; se houver perda de pacotes, os dados são corrompidos ou perdidos.
- ROS 2: Permite configurar políticas de QoS (ex: confiabilidade garantida, limite de histórico, prazos de entrega) para lidar com redes instáveis.

### Suporte a Sistemas e Multiplataforma

- ROS 1: Projetado essencialmente para Linux (Ubuntu).
- ROS 2: Oferece suporte nativo e multiplataforma para Linux, Windows e macOS

### Organização de Código

- ROS 1: Bibliotecas independentes para C++ (roscpp) e Python (rospy) com APIs diferentes.
- ROS 2: Possui uma biblioteca base em C (rcl), o que garante que as APIs para C++ (rclcpp) e Python (rclpy) sejam muito mais padronizadas e fáceis de usar