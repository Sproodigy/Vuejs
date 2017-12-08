<template>
  <div id="app">
<head>
<meta charset="utf-8">
<title>all</title>
</head>
<body>
   <!-- <div class="creature"></div> -->
   <div class="ch-wrap"></div>
   <button v-on:click="reverseMessage">Обратить порядок букв в сообщении</button>
 </body>
 <!-- <figure class="flip">
 <div class="flip-face front"><img src="//webref.ru/example/image/squirrel.jpg" alt="Белка"></div>
 <figcaption class="flip-face back">
<img src="http://www.factroom.ru/facts/wp-content/uploads/2014/02/Koshki-620x465.jpg" style="width: 250px; height: 273px">
 </figcaption>
</figure>
<div class="gallery">
 <figure class="left"><img src="//webref.ru/example/image/aquaria1.jpg" alt=""></figure>
 <figure class="center"><img src="//webref.ru/example/image/aquaria2.jpg" alt=""></figure>
 <figure class="right"><img src="//webref.ru/example/image/aquaria3.jpg" alt=""></figure>
</div>

<ul class="bar">
 <li>1</li><li>2</li>
 <li>3</li><li>4</li>
 <li>5</li><li>6</li>
 <li>7</li><li>8</li>
 <li>&darr;</li>
</ul> -->


</div>

</template>

<style>
.bar {
 top:-10em; right:3em; /* Положение */
 padding: .5em; /* Поля */
 margin: 0; /* Отступы */
 position: absolute; /* Абсолютное позиционирование */
 width: 1em; /* Ширина */
 background: #333; /* Цвет фона */
 color: #fff; /* Цвет текста */
 text-align: center; /* Выравнивание по центру */
 /* Переход */
 transition: top 1s ease-out 0.5s;
}
.bar:hover { top: 0; }


.gallery {
   text-align: center; /* Выравниваем по центру */
   perspective: 800px; /* Перспектива */
  }
  .gallery figure {
   margin: 0; /* Обнуляем отступы */
   display: inline-block; /* Выстраиваем по горизонтали */
   transform-style: preserve-3d; /* Вращаем в нужной плоскости */
  }
  .left {
   transform: rotateY(-30deg); /* Поворачиваем относительно оси Y */
   transform-origin: right center; /* Точка поворота справа */
  }
  .center {
   /* Поверх всех */
   position: relative; z-index: 2;
  }
  .right {
   transform: rotateY(30deg); /* Поворачиваем относительно оси Y */
   transform-origin: left center; /* Точка поворота слева */
  }
  .gallery img {
   transition: 4s; /* Время анимации */
  }
  .gallery img:hover {
   transform: rotateX(360deg); /* Вращаем на 360 градусов */
  }


.flip {
   position: relative; /* Относительное позиционирование */
   transform-style: preserve-3d; /* Вращение в 3D */
   width: 300px; height: 323px; /* Ширина и высота */
   transition: 3s; /* Время вращения */
  }
  .flip:hover {
   transform: rotateY(90deg); /* При наведении вращаем фото */
  }
  .flip-face {
   position: absolute; /* Абсолютное позиционирование */
   top: 0; bottom: 0; /* Задаём так равную высоту */
  }
  .flip-face.back {
   transform: rotateY(90deg);/* Вращаем по оси Y */
   backface-visibility: hidden; /* Скрываем обратную поверхность */
}

   .creature {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    background: #3ac;
    position: relative;
   }
   .creature::before, .creature::after {
    content: '';
    position: absolute;
    width: 30px;
    height: 50px;
    border-radius: 50%;
    background: #000;
    top: 60px;
    animation: eye 5s ease-in-out infinite;
    -webkit-animation: eye 5s ease-in-out infinite;
   }
   .creature::before { left: 85px; }
   .creature::after { right: 85px; }
   @keyframes eye {
    90% { transform: none; }
    95% { transform: scaleY(0.1); }
   }
   @-webkit-keyframes eye {
    90% { transform: none; }
    95% { transform: scaleY(0.1); }

  .ch-wrap {
    width: 400px;
    height: 400px;
    border: 1px solid #111;
  }
  .ch-item {
    width: 50px;
    height: 50px;
    float: left;
  }
  .ch-black {
    background: #111;
  }
  }
 </style>

<script>
   var chessWrap = document.querySelector('.ch-wrap');

    var i = 0, count = 0;

    while (count < 8 * 8) {
      var item = document.createElement('div');
      chessWrap.appendChild(item);

      item.classList.add('ch-item');

      if (i && i % 2)
        item.classList.add('ch-black')

      i += ((i + 2) % 9) ? 1 : 2;
      count++;
    }
</script>


<!-- // <script> -->
// export default {
//   name: 'app',
//   data () {
//     return {
//       msg: 'Добро пожаловать в Vue.js App' + new Date().toLocaleString()
//     }
//   }
// }
<!-- // </script> -->
