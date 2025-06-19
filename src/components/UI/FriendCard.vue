<template>
  <div class="friend-card">
    <img :src="avatar" alt="avatar" class="avatar" />
    <div class="info">
      <p class="name">{{ name }}</p>
      <p class="username">@{{ username }}</p>
      <p class="rating">Rating: {{ rating }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "FriendCard",
  props: {
    name: String,
    username: String,
    rating: Number,
    avatar: String,
  },
};
</script>

<style scoped>
.friend-card {
  display: flex;
  align-items: center;
  background-color: #2a2a3d;
  border-radius: 10px;
  padding: 12px;
  color: #fff;
  cursor: pointer;
}

.avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 12px;
}

.info {
  display: flex;
  flex-direction: column;
}

.name {
  font-weight: bold;
  margin: 0;
}

.username {
  font-size: 0.85rem;
  color: #bbb;
  margin: 2px 0;
}

.rating {
  font-size: 0.85rem;
  color: #ccc;
}
</style>
