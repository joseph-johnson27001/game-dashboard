<template>
  <nav class="top-nav">
    <div class="nav-content">
      <!-- Profile photo area -->
      <div class="profile-photo">
        <span class="profile-wrapper">
          <img
            src="https://randomuser.me/api/portraits/women/28.jpg"
            alt="User profile"
            width="35"
            height="35"
          />
          <span class="username">joanne01</span>
        </span>
      </div>

      <!-- Icon containers -->
      <div class="nav-items">
        <div class="nav-icon games" title="Games">
          <i class="fas fa-gamepad"></i>
        </div>
        <div class="nav-icon leaderboard" title="Leaderboard">
          <i class="fas fa-trophy"></i>
        </div>
        <div class="nav-icon home" title="Home">
          <i class="fas fa-home"></i>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "TopNav",
};
</script>

<style scoped>
.top-nav {
  flex-grow: 1;
  background-color: rgb(37, 41, 60);
  padding: 11px 15px;
  border-bottom: 1px solid #a1a0b66e;
}

.nav-content {
  margin: 0 auto;
  display: flex;
  align-items: center;
  color: #a1a0b6;
  justify-content: space-between;
}

.profile-photo .profile-wrapper {
  display: flex;
  align-items: center;
  gap: 7px;
}

.profile-photo img {
  border-radius: 50%;
  object-fit: cover;
  cursor: pointer;
  border: 1px solid #f3f3f3;
  display: block;
}

.username {
  color: #f3f3f3;
}

.nav-items {
  display: flex;
  align-items: center;
}

.nav-icon {
  padding: 0.5rem;
  border-radius: 8px;
  transition: background-color 0.2s ease;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-icon:hover {
  background-color: rgba(255, 255, 255, 0.05);
}

.nav-icon i {
  font-size: 1.3rem;
}

.nav-icon.games i {
  color: #60a5fa;
}

.nav-icon.leaderboard i {
  color: #facc15;
}

.nav-icon.home i {
  color: #d3346c;
}
</style>
