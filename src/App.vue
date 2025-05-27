<template>
  <div id="app">
    <div class="main"></div>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
body {
  margin: 0;
  background-color: rgb(37, 41, 60);
  display: flex;
  justify-content: center;
}

.main {
  width: 100dvw;
  height: 100dvh;
  max-width: 1200px;
  border-left: 1px solid rgba(255, 255, 255, 0.1);
  border-right: 1px solid rgba(255, 255, 255, 0.1);
}
</style>
