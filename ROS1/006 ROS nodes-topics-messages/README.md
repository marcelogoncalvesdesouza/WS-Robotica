[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)

## ROS nodes-topics-messages

### Nós
- Executáveis que realilizam alguma tarefa e compõem a aplicação
- Linguagens C++ ou Python
- Podem ser instanciados múltiplas vezes, garantindo modularidade
- Trocam informações por meio de messages, services ou actions

### Tópicos
- "Endereços" que os nós utilizam para a troca de mensagens
- Todo tópico possui um tipo de mensagem específica associada

### Mensagens
- Definidas por tipos de dados primitivos (int, float, string, bool, ...)
- Associação por múltiplos tipos e por vetores

Pacote de menssagens: std_msgs

#### Exemplos:
- std_msgs/Bool
- std_msgs/Int32
- geometry_msgs/Point
- nav_msgs/Path

[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)