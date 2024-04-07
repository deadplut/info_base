
установка webpack и ts-loader, чтобы webpack понимал TS
```
npm install --save-dev webpack webpack-cli
npm install --save-dev ts-loader
```


```
const path = require('path');

module.exports = {
    entry: './src/index.ts',
    module: {
        rules: [
            {
                test: /\.ts$/,
                use: 'ts-loader',
                exclude: /node_modules/,
            },
        ],
    },
    resolve: {
        extensions: ['.ts', '.js'],
    },
    output: {
        filename: 'main.js',
        path: path.resolve(__dirname, 'dist'),
    },
};
```

в `rules` - правила обработки
`extensions` - расширения, которые содержит wewbpack( `.ts` - typescript)




### Источники
[Яндекс.практикум](https://practicum.yandex.ru/learn/high-education-web-developer-magistr/courses/dcbe5700-0747-4b6d-aeec-7c089f3c8951/sprints/236862/topics/0d310721-f025-4b45-b235-bc858c43bdc6/lessons/14094b4e-17f8-4c33-b6b4-a3b209b206ee/)



### Тэги
#сборка_проекта 