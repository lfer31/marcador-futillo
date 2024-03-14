<template>
  <div id="app">
    <h1>Marcador de Fútbol</h1>
    <div class="team-input">
      <input v-model="team1.name" placeholder="Nombre del equipo 1">
      <input v-model="team2.name" placeholder="Nombre del equipo 2">
    </div>
    <div class="scoreboard">
      <div class="team">
        <h2>{{ team1.name || 'Equipo 1' }}</h2>
        <button @click="team1.score++">Gol</button>
        <h2>Goles: {{ team1.score }}</h2>
      </div>
      <div class="team">
        <h2>{{ team2.name || 'Equipo 2' }}</h2>
        <button @click="team2.score++">Gol</button>
        <h2>Goles: {{ team2.score }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      team1: {
        name: '',
        score: 0,
      },
      team2: {
        name: '',
        score: 0,
      },
    };
  },
};
</script>

<style>
#app {
  text-align: center;
  /* margin-top: 50px; */
}

.team-input input {
  margin: 20px;
  padding: 10px;
  font-size: 16px;
}

.scoreboard {
  display: flex;
  justify-content: center;
}

.team {
  width: 300px;
  margin: 20px;
  padding: 20px;
  border: 1px solid #000;
  border-radius: 15px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  margin-top: 10px;
  cursor: pointer;
}
</style>
