<template>
  <nav class="top-nav">
    <div class="nav-content">
      <div class="logo">ChessDash</div>
      
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
  padding: 0.75rem 1rem;
}

.nav-content {
  margin: 0 auto;
  display: flex;
  align-items: center;
  color: white;
  justify-content: space-between;
}

.logo {
  font-size: 1.25rem;
  font-weight: bold;
  font-family: 'Unica One';
}

.spacer {
  flex-grow: 1;
}

.nav-items a {
  color: white;
  text-decoration: none;
  margin-left: 1.5rem;
  font-size: 0.95rem;
}

</style>
