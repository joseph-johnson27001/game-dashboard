<template>
  <div id="app">
    <SideBar />
    <div class="main">
      <TopNav />
      <div class="content">
        <WelcomeBackSection />
        <GameArea />
        <FriendArea />
        <LearningArea />
        <GameHistory />
      </div>
    </div>
    <DashboardButton />
  </div>
</template>

<script>
import SideBar from "./components/Navigation/SideBar.vue";
import TopNav from "./components/Navigation/TopNav.vue";
// import WelcomeBackSection from "./components/Layout/WelcomeBackSection.vue";
import GameArea from "./components/Layout/GameArea.vue";
import LearningArea from "./components/Layout/LearningArea.vue";
import GameHistory from "./components/Layout/GameHistory.vue";
import FriendArea from "./components/Layout/FriendArea.vue";
import DashboardButton from "./components/UI/DashboardButton.vue";

export default {
  name: "App",
  components: {
    TopNav,
    SideBar,
    // WelcomeBackSection,
    GameArea,
    LearningArea,
    GameHistory,
    FriendArea,
    DashboardButton,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: "Assistant", sans-serif;
  background-color: rgb(21, 25, 41);
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
  margin-left: 65px;
}

.content {
  padding: 15px;
}

p {
  color: #e7e6f0;
  margin-top: 10px;
  margin-bottom: 10px;
}

@media screen and (max-width: 500px) {
  .main {
    margin-left: 0;
  }
}
</style>
