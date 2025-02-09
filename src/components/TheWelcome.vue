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
    Indiscutablement, Girier, plus connu sous le pseudo Leblanc9722, se distingue comme le joueur au niveau des plus décevants. Inlassablement, il multiplie les défaites et entraîne ses coéquipiers dans sa chute lors des parties multijoueurs. Tout joueur devrait rêver d’avoir la chance de l’affronter, car une victoire semble pratiquement garantie.
  </WelcomeItem>
</template>