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
        <div class="nav-icon" title="Games">
          <i class="fas fa-gamepad"></i>
        </div>
        <div class="nav-icon" title="Leaderboard">
          <i class="fas fa-trophy"></i>
        </div>
        <div class="nav-icon" title="Home">
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
  padding-bottom: 5px;
  border-bottom: 1px solid #a1a0b6;
  padding: 10px 15px;
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
  border: 1px solid #fff;
  display: block;
}

.username {
  color: #fff;

}

.nav-items {
  display: flex;
  gap: 0;
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
  color: #a1a0b6;
  font-size: 1.1rem;
}
</style>
