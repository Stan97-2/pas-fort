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
  <WelcomeItem>
    <template #heading>1. Théo GIRIER (Leblanc9722)</template>
    Indiscutablement, le joueur dont le niveau est le plus décevant, Girier, ne cesse de perdre et d'entraîner ses coéquipiers dans sa chute lors des parties multijoueurs. Tout joueur devrait espérer avoir la chance de l'affronter, car une victoire semble assurée.
  </WelcomeItem>
</template>