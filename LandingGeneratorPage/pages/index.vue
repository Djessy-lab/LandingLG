<template>
  <Saas v-if="currentConfig" v-bind="currentConfig" />
  <div v-else>Chargement...</div>
</template>

<script>
export default {
  name: 'page',
  data() {
    return {
      currentConfig: null
    };
  },
  async mounted() {
    try {
      this.currentConfig = await $fetch(`/api/getConfig?configName=LandingGenerator`);
    } catch (error) {
      console.error('Erreur lors du chargement de la configuration:', error);
    }
  }
}
</script>
