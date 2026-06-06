[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)

## Criando um ROS Workspace

<b>Espaço de trabalho (<i>catkin_ws<i>)</b>
- Pacotes: um package é como uma aplicação ROS é feita;
- Cada pacote pode possuir uma ou mais aplicações que utiliza uma ou mais de uma linguagem;
- A workspace é onde ficam os packages.

<b>Estrutura de um WS</b>
- build: arquivos compilados;
- devel: variáveis de ambiente;
- src: pacotes e aplicações.

## Exemplo
- Dentro do /home criar a estrutura para o workspace:
```
mkdir catkin_ws && cd catkin_ws && mkdir src && cd src
```
- Voltar para WS e compilar
```
catkin_make
```
Obs.: para compilar apenas m pacote dentro do WS utilizar --only-pkg-with-deps pkName

- source devel/setup.bash (o sistema reconhece a ws quando abrir um novo terminal)