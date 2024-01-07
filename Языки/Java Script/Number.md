
Тип данных содержит числа и бесконечность(+-Infinity) и пустоту(NaN - not a number)

для проверки на бесконечность используют метод: 
`Number.isFinite`

```
Number.isFinite(Infinity); // false
Number.isFinite(-Infinity); // false
Number.isFinite(1703); // true
```


При делении на ноль будет `NaN`, Также `NaN` !=== `Nan`
Для проверки на отсутсвия числа используют Nan:

```
Number.isNaN(NaN); // true
Number.isNaN(0 / 0); // true
```






### Тэги

#тип_данных 