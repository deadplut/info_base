Конструкция dataclass упрощает создание Class в python, в себе уже содержит стандартные методы при объявлении класса: `__init__`, `__repr__` и `__eq__`

аналогом является NamedTuple из [[Именнованне кортежи|именнованных кортежей]]

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

Чтобы задать значение по умолчанию и другие параметры необходимо использовать ф-цию `field` с нужными опциями

```
@dataclass 
class Coordinate: 
	x: int 
	y: int = field(default=False, repr=False)
	z: list = field(defaulfactory=list) # для создания пустого списка

```


другие опции:
`init`, `repr`, `compare`, `hash`, `metadata`

##### post_init

Для выполнения действий сразу после init стоит использовать post_init


##### Для создания параметра, который не будет использоваться в классе

Нужно использовать InitVar:

```
@dataclass 
class Coordinate: 
	x: int 
	y: InitVar[int] = Non

	def __post_init__(self, y):
		if not y:
			print('ass')
```

##### <span style="background:#ff4d4f">Важно</span> 
Не надо передавать в значения по умолчанию изменяемы типы данных списки, [[Множества]], [[Языки/Python/Словари|Словари]], так они могут привести к некорректному значению.

стоит использовать фабрику для создания таких объектов.

#### Ссылки
https://pythonru.com/osnovy/dataclass-v-python
