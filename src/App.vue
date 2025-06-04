<template>
  <div id="app">
    <SideBar />
    <div class="main">
      <TopNav />
      <div class="content">
      <WelcomeBackSection />
      <UserStatistics />
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from './components/Navigation/SideBar.vue';
import TopNav from './components/Navigation/TopNav.vue';
import WelcomeBackSection from './components/Layout/WelcomeBackSection.vue';
import UserStatistics from './components/Layout/UserStatistics.vue';

export default {
  name: "App",
  components: {
    TopNav,
    SideBar,
    WelcomeBackSection,
    UserStatistics,
  }
};
</script>

<style>
body {
  margin: 0;
  font-family: 'Assistant', sans-serif;
   background-color: rgb(37, 41, 60);
}

#app {
  display: flex;
  height: 100dvh;
  width: 100%;
  background-color: rgb(37, 41, 60);
  height: 100%;
}



.main {
  width: 100%;
  flex-grow: 1;
}

.content {
  padding: 15px;
}

p {
  color: #a1a0b6;
}
</style>
