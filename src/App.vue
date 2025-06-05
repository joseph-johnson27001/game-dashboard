<template>
  <div id="app">
    <SideBar />
    <div class="main">
      <TopNav />
      <div class="content">
        <WelcomeBackSection />
        <UserStatistics />
        <GameArea />
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from "./components/Navigation/SideBar.vue";
import TopNav from "./components/Navigation/TopNav.vue";
import WelcomeBackSection from "./components/Layout/WelcomeBackSection.vue";
import UserStatistics from "./components/Layout/UserStatistics.vue";
import GameArea from "./components/Layout/GameArea.vue";

export default {
  name: "App",
  components: {
    TopNav,
    SideBar,
    WelcomeBackSection,
    UserStatistics,
    GameArea,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: "Assistant", sans-serif;
  background-color: rgb(37, 41, 60);
  min-height: 100dvh;
}

#app {
  display: flex;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.main {
  flex-grow: 1;
  min-width: 0;
  overflow: auto;
}

.content {
  padding: 15px;
}

p {
  color: #a1a0b6;
}
</style>
