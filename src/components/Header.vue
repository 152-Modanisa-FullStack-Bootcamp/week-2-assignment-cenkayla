<template>
    <div class="header">
      <button @click="navigateToFavoritePage" class="favorites">Favorites</button>
    </div>
</template>

<script>

export default {
  name: 'Header',
  methods: {
    navigateToFavoritePage() {
      this.$router.push({name:"Favorites", params: {userid: "bootcamp"}})
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  width: 100%;
  height: 70px;
  background-color: red;
  position: relative;
}
.favorites {
  position: absolute;
  width: 75px;
  height: 30px;
  top: 20px;
  right: 15px;
}
</style>
