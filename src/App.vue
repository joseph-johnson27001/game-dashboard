<template>
  <div id="app">
    <div class="main">
      <TopNav />
    </div>
  </div>
</template>

<script>
import TopNav from './components/Navigation/TopNav.vue';

export default {
  name: "App",
  components: {
    TopNav,
  }
};
</script>

<style>
body {
  margin: 0;
  background-color: rgb(37, 41, 60);
  display: flex;
  justify-content: center;
  font-family: 'Assistant', sans-serif;
}

.main {
  width: 100dvw;
  height: 100dvh;
  max-width: 1200px;
}
</style>
