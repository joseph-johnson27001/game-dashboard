<template>
  <div id="app">
    <SideBar />
    <div class="main">
      <TopNav />
      <div class="content">
        <WelcomeBackSection />
        <GameArea />
        <LearningArea />
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from "./components/Navigation/SideBar.vue";
import TopNav from "./components/Navigation/TopNav.vue";
import WelcomeBackSection from "./components/Layout/WelcomeBackSection.vue";
import GameArea from "./components/Layout/GameArea.vue";
import LearningArea from "./components/Layout/LearningArea.vue";

export default {
  name: "App",
  components: {
    TopNav,
    SideBar,
    WelcomeBackSection,
    GameArea,
    LearningArea,
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
  color: #d8d7e5;
  margin-top: 10px;
  margin-bottom: 10px;
}
</style>
