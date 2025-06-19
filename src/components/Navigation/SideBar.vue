<template>
  <aside class="sidebar">
    <nav class="sidebar-nav">
      <div class="nav-item toggle-container">
        <div class="icon-container toggle-btn">
          <i class="fas fa-bars icon"></i>
        </div>
        <span class="label sidebar-header">ChessDash</span>
      </div>

      <a href="#">
        <div class="icon-container">
          <i class="fas fa-home icon blitz"></i>
        </div>
        <span class="label">Dashboard</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-chess-knight icon bullet"></i>
        </div>
        <span class="label">Games</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-chart-line icon rapid"></i>
        </div>
        <span class="label">Stats</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-user-friends icon friends"></i>
        </div>
        <span class="label">Social</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-trophy icon tournaments"></i>
        </div>
        <span class="label">Tournaments</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-user-circle icon profile"></i>
        </div>
        <span class="label">Profile</span>
      </a>
      <a href="#">
        <div class="icon-container">
          <i class="fas fa-cogs icon puzzles"></i>
        </div>
        <span class="label">Settings</span>
      </a>
    </nav>

    <!-- Logout Button -->
    <div class="logout-btn">
      <div class="icon-container">
        <i class="fas fa-sign-out-alt icon logout"></i>
      </div>
      <span class="label">Logout</span>
    </div>
  </aside>
</template>

<script>
export default {
  name: "SideBar",
};
</script>

<style scoped>
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 45px;
  height: 100vh;
  background-color: rgb(21, 25, 41);
  color: white;
  z-index: 1000;
  overflow: hidden;
  transition: width 0.3s ease;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 15px 10px;
  border-right: 1px solid #a1a0b66e;
  font-family: "Inter", sans-serif;
}

.sidebar:hover {
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

.icon-container {
  width: 28px;
  height: 28px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
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

.sidebar:hover .label {
  opacity: 1;
  visibility: visible;
}

.toggle-container {
  padding-bottom: 0px;
  color: white;
}

.sidebar-header {
  font-family: "Unica One", sans-serif;
  font-size: 1.4rem;
}

.logout-btn {
  display: flex;
  align-items: center;
  padding: 0.5rem 0.5rem 40px 0.5rem;
  cursor: pointer;
  color: #fff;
  transition: color 0.2s ease;
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
.logout {
  color: #d45252;
}

@media screen and (max-width: 500px) {
  .sidebar {
    display: none;
  }
}
</style>
