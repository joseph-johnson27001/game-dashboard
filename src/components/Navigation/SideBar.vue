<template>
  <aside class="sidebar">
    <div class="sidebar-header">Menu</div>
    <nav class="sidebar-nav">
      <a href="#">🏠 Dashboard</a>
      <a href="#">🎮 Games</a>
      <a href="#">📊 Stats</a>
      <a href="#">⚙️ Settings</a>
    </nav>
  </aside>
</template>

<script>
export default {
  name: "SideBar",
};
</script>

<style scoped>
.sidebar {
  width: 200px;
  max-width: 200px;
  flex-shrink: 0;
  height: 100dvh;
  background-color: rgb(30, 33, 50);
  color: white;
  display: flex;
  flex-direction: column;
  padding: 1rem;
  box-shadow: 2px 0 4px rgba(0, 0, 0, 0.3);
}

.sidebar-header {
  font-family: 'Unica One', cursive;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}

.sidebar-nav {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.sidebar-nav a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
}

</style>
