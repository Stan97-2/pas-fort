<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <div class="ranking-container">
    <h2 class="ranking-title">Classement</h2>
    <ul class="ranking-list">
      <li v-for="(member, index) in ranking" :key="index" class="ranking-item">
        <div class="member-photo">
          <img :src="member.photo" :alt="member.name" />
        </div>
        <div class="member-info">
          <span class="member-rank">{{ index + 1 }}. </span>
          <span class="member-name">{{ member.name }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ranking: [
        { name: 'Membre 1', photo: 'https://placekitten.com/100/100' },
        { name: 'Membre 2', photo: 'https://placekitten.com/101/101' },
        { name: 'Membre 3', photo: 'https://placekitten.com/102/102' },
        { name: 'Membre 4', photo: 'https://placekitten.com/103/103' }
      ]
    };
  }
};
</script>

<style scoped>
.ranking-container {
  background-color: black;
  color: white;
  padding: 20px;
  border-radius: 8px;
  max-width: 400px;
  margin: auto;
}

.ranking-title {
  text-align: center;
  font-size: 24px;
  margin-bottom: 20px;
}

.ranking-list {
  list-style-type: none;
  padding: 0;
}

.ranking-item {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.member-photo img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 15px;
}

.member-info {
  display: flex;
  align-items: center;
}

.member-rank {
  font-weight: bold;
}

.member-name {
  font-size: 18px;
}
</style>
