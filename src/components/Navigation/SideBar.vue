<template>
  <aside class="sidebar">
    <div class="sidebar-header">ChessDash</div>
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
  width: 150px;
  max-width: 200px;
  flex-shrink: 0;
  height: 100dvh;
  background-color: rgb(37, 41, 60);
  color: white;
  display: flex;
  flex-direction: column;
  padding: 1rem;
  border-right: 1px solid #a1a0b6;
}

.sidebar-header {
  font-family: 'Unica One', cursive;
  font-size: 1.5rem;
  margin-bottom: 15px;
  color: #c1bfd6
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
