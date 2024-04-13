
### Определение
`this` - контекст - объекты окружения, может быть глобальными, метода


```
#Контекст метода
const grandma = {
  name: 'Бабушка Люба',

  cookPancakes: function() {
    console.log(this.name, 'напекла блинов — все за стол!', '😋');
  },
  makeMethod()
}

function makeMethod() {
	console.log(this.name). # будет работать
	console.log('Если вызвать внутри объекта, то контекст подхватится')
}

grandma.cookPancakes();
// Бабушка Люба напекла блинов — все за стол! 😋

grandma.makeMethod(); 
// 'Бабушка Люба'
```


- Контекст ограничен своей областью: Так при объявлении во вложенном объекте он выведет `undefined`
- [[Стрелочные функции|Стрелочные фуникции]], объявленные как вложенный объект, также не видят переменные извне



### Привязка
метод `.bind` - создает ф-цию обертку, в которой запустится исходная функция и заданный контекст

```
function celebrateBirthday(...invited) {
  console.log(this.name, 'сегодня отмечает день рождения!', '🥳');

  if (invited.length) {
    console.log('На праздник приглашены:', invited.join(', '));
  }
}

const grandma = {
  name: 'Бабушка Люба'
}

const celebrateGrandmaBirthday = celebrateBirthday.bind(grandma);

celebrateGrandmaBirthday('папа', 'мама', 'я', 'сестра');

# или так bind позваляет указать часть или все аргументы

celebrateGrandmaBirthday = celebrateBirthday.bind(grandma, 'папа', 'мама');

celebrateGrandmaBirthday('я', 'сестра');

```

метод `.apply`  позволяет сделать тоже самое, но аргументы ф-ции передать массивом

```
celebrateBirthday.apply(grandma, ['папа', 'мама', 'я', 'сестра']);
// Бабушка Люба сегодня отмечает день рождения! 🥳
// На праздник приглашены: папа, мама, я, сестра
```





### Источники

[Яндекс.Практикум](https://practicum.yandex.ru/learn/high-education-web-developer-magistr/courses/dcbe5700-0747-4b6d-aeec-7c089f3c8951/sprints/236862/topics/66851ca6-9f92-4558-9edd-f30d13cdd317/lessons/45966c5b-5b22-4212-b634-9ceb36d7ef16/)


### Тэги

#ооп 