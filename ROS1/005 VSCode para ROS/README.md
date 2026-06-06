[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)

## Configuração para o ROS

### Extensões
- ms-python.python
- ms-vscode.cpptools
- twxs.cmake

### Abrir o src do ws: ctrl+shift+p e acessar o c_cpp_properties.json: C/C++: Edit Configurations (UI)

- No includePath adicionar:
```
[
    "${workspaceFolder}/**",
    "/opt/ros/noetic/include",
    "~/catkin_ws/devel/include"
]
```
- No cppStandart adicionar:
```
    "c++14"
```

[Voltar](https://github.com/marcelogoncalvesdesouza/WS-Robotica/tree/main/ROS1)