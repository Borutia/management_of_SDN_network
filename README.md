# Management_of_SDN_network
Построения сети управления в SDN сети

# Зависимости
Для работы приложения необходима версия языка Python 3.6 и выше.
Все библиотеки испульзуются стандартные. 

# Запуск
Программа принимает на вход путь к файлу в формате GraphML, 
дополнительный парамерты k1 и k2. 

Пример запуска программы:

```
>>> python3 ./main.py -t tests/AttMpls.graphml -k1 3 -k2 22
Parsed arguments:
destination_node_id = 22
file_name = tests/AttMpls.graphml
source_node_id = 3
Parsed 25 nodes
Parsed 114 edges
Parsed graph: G(25 nodes, 114 edges)
Written topology to file tests/AttMpls.graphml_topo.csv
Written routes to file tests/AttMpls.graphml_routes.csv
Visualization available at file tests/AttMpls.graphml_demo.html

```

Программа генерирует два csv файла и, если указаны параметры -k1 и -k2, 
один HTML файл с визуализацией графа. 
Прямой путь обозначается черным, резервный - красным.

Для вычисления расстояния между двумя точками, заданными в координатах, 
используется формула:
[greate-circle distance](https://en.wikipedia.org/wiki/Great-circle_distance).

# Визуализация графа
![alt text](image/graph.png "www.topology-zoo.org, ATT North America")