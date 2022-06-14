<template>
<div id="app">
  <TopNav/>
  <div class="app-container">
    <Nuxt />
  </div>
  <bottom-nav/>
</div>
</template>

<script>
import BottomNav from '../components/BottomNav.vue'
import TopNav from '../components/TopNav.vue'
export default {
  components: { BottomNav, TopNav },
  name: 'IndexPage'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Arimo&family=Gamja+Flower&family=Inter&family=Montserrat&family=Roboto&display=swap');
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.app-container{
  margin: 64px 0;
}
</style>
