<template>
  <ul>
      <cronoItem v-for="patata in patataList" :key="patata.id" :title="patata.name" :description="patata.description" :relevant="patata.relevant" />    
  </ul>
</template>

<script>
import cronoItem from "./CronoItem.vue";
export default {
  name: "cronoList",
  props: ["patataList"],
  components: {
    cronoItem,
  },
};
</script>

<style scoped>
</style>