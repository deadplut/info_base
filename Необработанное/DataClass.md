Конструкция dataclass упрощает создание Class в python, в себе уже содержит стандартные методы при объявлении класса: `__init__`, `__repr__` и `__eq__`

Также поддерживает и остальные методы, которые можно включить опционально


```
from dataclasses import dataclass 

@dataclass 
class Coordinate: 
	x: int 
	y: int 
	z: int 


a = Coordinate(4, 5, 3)
```

#### Ссылки
https://pythonru.com/osnovy/dataclass-v-python
