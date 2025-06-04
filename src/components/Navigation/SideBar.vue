<template>
  <aside class="sidebar">
    <div class="sidebar-header">ChessDash</div>
    <nav class="sidebar-nav">
      <a href="#">
        <i class="fas fa-home icon blitz"></i>
        <span class="label">Dashboard</span>
      </a>
      <a href="#">
        <i class="fas fa-chess-knight icon bullet"></i>
        <span class="label">Games</span>
      </a>
      <a href="#">
        <i class="fas fa-chart-line icon rapid"></i>
        <span class="label">Stats</span>
      </a>
      <a href="#">
        <i class="fas fa-cogs icon puzzles"></i>
        <span class="label">Settings</span>
      </a>
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
  width: 45px;
  height: 100dvh;
  background-color: rgb(37, 41, 60);
  color: white;
  display: flex;
  flex-direction: column;
  padding: 1rem 0.5rem;
  border-right: 1px solid #a1a0b66e;
  transition: width 0.3s ease;
  overflow: hidden;
  position: relative;
}

.sidebar:hover {
  width: 150px;
}

.sidebar-header {
  font-family: 'Unica One', cursive;
  font-size: 1.2rem;
  margin-bottom: 20px;
  color: #c1bfd6;
  text-align: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.sidebar:hover .sidebar-header {
  opacity: 1;
}

.sidebar-nav {
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
}

.sidebar-nav a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 0.4rem 0.5rem;
  transition: color 0.2s ease;
  white-space: nowrap;
}

.sidebar-nav a:hover {
  color: #e5e7eb;
}

.icon {
  font-size: 1.4rem;
  min-width: 24px;
  text-align: center;
}

/* Initially hide labels */
.label {
  opacity: 0;
  transition: opacity 0.2s ease, transform 0.2s ease;
  transform: translateX(-5px);
}

/* Show labels on hover */
.sidebar:hover .label {
  opacity: 1;
  transform: translateX(0);
}

/* Color styles from rating cards */
.blitz {
  color: #facc15;
}
.bullet {
  color: #60a5fa;
}
.rapid {
  color: #34d399;
}
.puzzles {
  color: #f472b6;
}
</style>
