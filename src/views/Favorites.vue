<template>
  <div>
    <div class="header">
      <button @click="navigateToFavoritePage" class="favorites-page">
        Favorites
      </button>
    </div>
    <div class="favorites">
      <Card v-for="item in favorites" :key="item.id" :video="item"></Card>
    </div>
  </div>
</template>

<script>
import Card from "@/components/Favorites.vue";

export default {
  name: "Favorites",
  props: ["favorites"],
  components: {
    Card,
  },
};
</script>

<style scoped>
.favorites-page {
  width: 75px;
  height: 30px;
  margin-top: 20px;
  margin-right: 15px;
  margin-left: auto;
}
.header {
  width: 100%;
  height: 70px;
  background-color: red;
  display: flex;
}
</style>
