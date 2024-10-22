<template>
  <Saas v-if="currentConfig" v-bind="currentConfig" />
  <div v-else>Chargement en cours...</div>
</template>

<script>
import config from "@/data/config";
export default {
  name: "page",
  data() {
    return {
      config,
      currentConfig: null,
    };
  },
  mounted() {
    this.currentConfig = config.LandingGenerator;
  },
};
</script>
