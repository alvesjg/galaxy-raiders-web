<template>
    <div id="tela">
      <h1 id="titulo" >Leaderboard</h1>

      <div id="centralizacao">
        <table>
          <thead>
            <tr>
              <th>Data e Hora</th>
              <th>Asteroides Destruídos</th>
              <th>Pontuação</th>
            </tr>
          </thead>
          <tbody>
            <!-- Loop para exibir os dados do leaderboard -->
            <tr v-for="(entry, index) in leaderboardData" :key="index">
              <td>{{ formatDateTime(entry.dateTime) }}</td>
              <td>{{ entry.numberDestroyedAsteroids }}</td>
              <td>{{ entry.score }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </template>
  
  <script setup>
  import leaderboardData from './leaderboard.json';
  
  const formatDateTime = (dateTime) => {
    const dt = new Date(dateTime);
    return dt.toLocaleString();
  };
  </script>
  
  <style>
  /* Estilos para a tabela */
  table {
    width: 90%;
    border-collapse: collapse;
    border: 1px solid #ddd;
  }

  #titulo{
    text-align: center;
    margin: 50px 0;
  }
  
  
  #tela{
    font-family: 'Courier New', Courier, monospace;
    font-size: 30px;
    background-color: black;
    height: 100vh;
    position: fixed;
    width: 100%;
    color: white;
  }
  
  #centralizacao{
    display: flex;
    justify-content: center;
  }
  
  th, td {
    padding: 12px;
    text-align: left;
    border-bottom: 1px solid #ddd;
  }
  </style>
  