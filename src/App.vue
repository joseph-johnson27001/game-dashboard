<template>
  <div id="app">
    <SideBar />
    <div class="main">
      <TopNav />
      <WelcomeBackSection />
    </div>
  </div>
</template>

<script>
import SideBar from './components/Navigation/SideBar.vue';
import TopNav from './components/Navigation/TopNav.vue';
import WelcomeBackSection from './components/UI/WelcomeBackSection.vue';

export default {
  name: "App",
  components: {
    TopNav,
    SideBar,
    WelcomeBackSection
  }
};
</script>

<style>
#app {
  display: flex;
  height: 100dvh;
  width: 100%;
  background-color: rgb(37, 41, 60);
}

body {
  margin: 0;
  font-family: 'Assistant', sans-serif;
}

.main {
  width: 100%;
  padding: 15px;
  flex-grow: 1;
}
</style>
