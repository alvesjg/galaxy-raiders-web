<template>


  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
  </head>
  <body>

    <div id="divisao_botao">
      <a href="leaderboard"> LEADERBOARD</a>
      <a href="play">JOGAR</a>
      <a href="http://www.google.com">FECHAR</a>
    </div>
  </body>
</template>


<style>

#divisao_botao{

  font-family: 'Courier New', Courier, monospace;
  height: 100%;
  background-image: url(../assets/space.gif);
  background-repeat: no-repeat;
  background-size: cover;

  display: flex;
  position: fixed;
  justify-content: space-around;
  width: 100%;
  margin: auto;
}

a{
  color: black;
  height: 500px;
  width: 400px;
  margin: auto;
  border-radius: 20px;
  background-color: rgba(236, 236, 236, 0.9);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 40px;
  transition: 0.5s;
  text-decoration-line: none;
}

a:hover{
  background-color: rgba(180, 180, 180, 0.9);
  transition: 0.5s;
}


</style>
<script>
</script>