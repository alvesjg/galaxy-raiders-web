<template>
    <div>
      <h1>Leaderboard</h1>
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
    width: 100%;
    border-collapse: collapse;
    border: 1px solid #ddd;
  }
  
  th, td {
    padding: 12px;
    text-align: left;
    border-bottom: 1px solid #ddd;
  }
  
  th {
    background-color: #f2f2f2;
  }
  </style>
  