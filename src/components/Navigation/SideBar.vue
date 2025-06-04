<template>
  <aside :class="['sidebar', { expanded: isExpanded }]">
    <nav class="sidebar-nav">
      <div class="nav-item toggle-container" @click="toggleSidebar" role="button" tabindex="0" aria-label="Toggle sidebar">
        <div class="icon-container toggle-btn">
          <i class="fas fa-bars icon"></i>
        </div>
        <span class="label sidebar-header" :class="{ visible: isExpanded }">ChessDash</span>
      </div>

      <a href="#">
        <div class="icon-container">
          <i class="fas fa-home icon blitz"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Dashboard</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-chess-knight icon bullet"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Games</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-chart-line icon rapid"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Stats</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-user-friends icon friends"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Friends</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-trophy icon tournaments"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Tournaments</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-user-circle icon profile"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Profile</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-question-circle icon help"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Help</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-cogs icon puzzles"></i>
        </div>
        <span class="label" :class="{ visible: isExpanded }">Settings</span>
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
  padding: 15px 10px;
  border-right: 1px solid #a1a0b66e;
  overflow: hidden;
  position: relative;
  font-family: "Inter", sans-serif;
}

.sidebar.expanded {
  width: 180px;
}

.sidebar-nav {
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.nav-item,
.sidebar-nav a {
  color: #fff;
  font-size: 0.9rem;
  font-weight: 100;
  display: flex;
  align-items: center;
  padding: 0.2rem 0.5rem;
  cursor: pointer;
  white-space: nowrap;
  user-select: none;
  transition: color 0.2s ease;
  text-decoration: none;
}

.nav-item:hover,
.sidebar-nav a:hover {
  color: #e5e7eb;
}

.icon-container {
  width: 28px;
  height: 28px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.toggle-btn {
  cursor: pointer;
}

.icon {
  font-size: 1.4rem;
}

.label {
  margin-left: 8px;
  opacity: 0;
  visibility: hidden;
  transition: opacity 0.3s ease;
  user-select: none;
}

.label.visible {
  opacity: 1;
  visibility: visible;
}

.toggle-container {
  padding-bottom: 0px;
  color: white;
}

.sidebar-header {
  font-family: 'Unica one', sans-serif;
  font-size: 1.4rem;
 
}

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

.friends {
  color: #f97316;
}

.tournaments {
  color: #8b5cf6;
}

.profile {
  color: #3b82f6;
}

.help {
  color: #6b7280;
}
</style>
