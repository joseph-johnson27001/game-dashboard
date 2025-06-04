<template>
  <aside :class="['sidebar', { expanded: isExpanded }]">
    <div class="sidebar-header">
      <span class="site-label" v-if="isExpanded">ChessDash</span>
      <button class="toggle-btn" @click="toggleSidebar" aria-label="Toggle sidebar">
        <i class="fas fa-bars"></i>
      </button>
    </div>

    <nav class="sidebar-nav">
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-home icon blitz"></i>
        </div>
        <span class="label" v-if="isExpanded">Dashboard</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-chess-knight icon bullet"></i>
        </div>
        <span class="label" v-if="isExpanded">Games</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-chart-line icon rapid"></i>
        </div>
        <span class="label" v-if="isExpanded">Stats</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-cogs icon puzzles"></i>
        </div>
        <span class="label" v-if="isExpanded">Settings</span>
      </a>
    </nav>
  </aside>
</template>

<script>
export default {
  name: "SideBar",
  data() {
    return {
      isExpanded: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.isExpanded = !this.isExpanded;
    },
  },
};
</script>

<style scoped>
.sidebar {
  width: 45px;
  transition: width 0.3s ease;
  height: 100dvh;
  background-color: rgb(37, 41, 60);
  color: white;
  display: flex;
  flex-direction: column;
  padding: 20px 10px;
  border-right: 1px solid #a1a0b66e;
  overflow: hidden;
  position: relative;
}

.sidebar.expanded {
  width: 150px;
}

.sidebar-header {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-family: 'Unica One', cursive;
  font-size: 1.2rem;
  margin-bottom: 20px;
  color: #c1bfd6;
  justify-content: center;
}

.toggle-btn {
  background: none;
  border: none;
  color: white;
  font-size: 1.2rem;
  cursor: pointer;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: center;
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

/* Fixed size for icons */
.icon-container {
  width: 28px;
  height: 28px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon {
  font-size: 1.4rem;
}

/* Color styles */
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
