Функция модуля functools, принимает [[Итерируемый объект]], возвращает неитерируемый объект(одиночный результат)


Данные две функции эквивалентны;
```
from functools import reduce  
  
r = reduce((lambda x, y: x + y), [-1, 0, 1, 2, 3, 4])  
print(r)  
  
def myreduce(func, sequence):  
    result = sequence[0]  
    for i in sequence[1:]:  
        result = func(result, i)  
  
    return result  
  
print(myreduce((lambda x, y: x + y),[-1, 0, 1, 2, 3, 4] ))
```

#функции