<template>
  <div id="app">
     <head>
      <meta charset="utf-8">
      <title>align-content</title>
     </head>
     <body>
      <div class="flex-cont">
       <div class="yellow"></div>
    </div>
      <div class="flex-contain">
       <div class="red"></div>
       <div class="yellow"></div>
       <div class="green"></div>
      </div>
     </body>
  </div>
</template>

<style>
 .flex-contain {
  width: 100px;
  height: 290px;
  border: 2px solid #333;
  margin: 30px;
  padding: 30px;
  /*display: flex;*/
  /*flex-wrap: wrap;*/
  align-content: center;
 }

 .flex-contain div {
  width: 90px; height: 90px;
  border-radius: 90%;
 }

 .flex-cont div {
  width: 50px; height: 50px;
  border-radius: 40%;
 }

  .flex-cont {
    padding: 30px;
    background: blue;
    flex-wrap: flex;
    display: flex;
    align-content: flex-end;
    width: 190px; height: 90px;
    border: 4pt dotted yellow;
    border-radius: 40%;
 }

 .red { background: magenta; }
 .yellow { background: yellow; }
 .green { background: green; }
</style>

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
