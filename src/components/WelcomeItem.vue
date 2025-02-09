<template>
  <div class="ranking-container">
    <h2 class="ranking-title">Classement</h2>
    <ul class="ranking-list">
      <li v-for="(player, index) in players" :key="player.id" class="ranking-item">
        <span class="ranking-position">{{ index + 1 }}</span>
        <img :src="player.photo" alt="photo" class="ranking-photo" />
        <div class="ranking-info">
          <p class="ranking-name">{{ player.name }}</p>
          <p class="ranking-score">Score: {{ player.score }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      players: [
        {
          id: 1,
          name: "Joueur 1",
          score: 100,
          photo: "https://via.placeholder.com/40"
        }
      ]
    };
  }
};
</script>

<style scoped>
.ranking-container {
  width: 100%;
  max-width: 400px;
  margin: auto;
  background: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  overflow: hidden;
}

.ranking-title {
  text-align: center;
  background: #333;
  color: white;
  padding: 10px;
  font-size: 20px;
  font-weight: bold;
}

.ranking-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.ranking-item {
  display: flex;
  align-items: center;
  padding: 10px;
  border-bottom: 1px solid #ddd;
}

.ranking-position {
  font-size: 18px;
  font-weight: bold;
  width: 30px;
  text-align: center;
}

.ranking-photo {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  object-fit: cover;
  margin: 0 10px;
}

.ranking-info {
  flex: 1;
}

.ranking-name {
  font-weight: bold;
}

.ranking-score {
  color: gray;
  font-size: 14px;
}
</style>
