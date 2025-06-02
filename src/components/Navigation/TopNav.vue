<template>
  <nav class="top-nav">
    <div class="nav-content">
      <!-- Profile photo area -->
      <div class="profile-photo">
        <img
          src="https://i.pravatar.cc/40" 
          alt="User profile"
          width="35"
          height="35"
        />
      </div>

      <div class="nav-items">
        <a href="#">Home</a>
        <a href="#">Games</a>
        <a href="#">Leaderboard</a>
        <a href="#">Profile</a>
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
  padding: 0.75rem 0;
  background-color: rgb(37, 41, 60);
}

.nav-content {
  margin: 0 auto;
  display: flex;
  align-items: center;
  color: white;
  justify-content: space-between;
  max-width: 1200px;
}

.profile-photo img {
  border-radius: 50%;
  object-fit: cover;
  display: block;
  cursor: pointer;
  border: 1px solid white;
}

.nav-items a {
  color: white;
  text-decoration: none;
  margin-left: 1.5rem;
  font-size: 0.95rem;
}
</style>
