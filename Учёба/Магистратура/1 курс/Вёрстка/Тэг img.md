Для вставки изображений


Аттрибут `loading="lazy"` - для lazy загрузки при наведении на изображение



Аттрибут srcset для указания ссылок на картинки под разные масштабы
```
<img src="flower.jpg"
  srcset="flower.jpg 1x,
          flower-2x.jpg 2x,
          flower-3x.jpg 3x"
    alt="Букет ярких роз крупным планом"
>
```



Или можно при помощи тэга \<picture>
```
<picture>
  <source srcset="flowers.avif" type="image/avif">
  <source srcset="flowers.webp" type="image/webp">
  <img src="flowers.jpeg" alt="Букет ярких роз крупным планом">
</picture>
```


Или при помощи image-set() в css
```
div {
    background-image: image-set(
    url("flowers.jpeg") 1x,
    url("flowers-2x.jpeg") 2x);
}
```