
Сортировка - размещение элементов данных в каком-либо порядке( ASC, DESC)

1. N - количество элемнтов
2. До какой степени элементы можно отсортировать


#### Основные критерии оценки
- количество необходимых сравнений С(N) : от макс N<sup>2</sup> до  минимального N(log<sub>2</sub>N) 
- Объем используемой памяти


Объем используемой памяти высчитывается по формуле:
`F = S(N) / ( S(N) + dS(N) )`

`S(N)` - объём памяти, занимаемой элементами данных до сортировки;
`dS(N)` - объём доп памяти

   
#### Дополнительные Критерии оценки:

**Устойчивость** - обращение внимания на сортировку одинаковых элементы.

**Естественность**   поведения - эффективность метода при сортировке уже упорядоченных или частично упорядоченных данных.  Если алгоритм учитывает характеристику входной последовательности и работает эффективнее, то алгоритм ведёт себя естественно.



#### Приёмы сортировок

1. [[Сортировка методом выборки|Выборки]]
2. [[Сортировка методом включения(вставки)|Вставки]]
3. [[Сортировка методом обмена|Обмен]]
4. [[Сортировка распредлением|Распределение]]
5. [[Сортировки на основе бинарных деревьев|Бинарные деревья]]
6. слияние

![[Pasted image 20240301224638.png]]





### Тэги

#сортировки
