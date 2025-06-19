<template>
  <div class="friend-card">
    <img :src="avatar" alt="avatar" class="avatar" />
    <div class="info">
      <p class="name">{{ name }}</p>
      <p class="username">@{{ username }}</p>
      <p class="rating">Rating: {{ rating }}</p>
    </div>
    <div class="actions">
      <i class="fas fa-chess-board" title="Challenge"></i>
      <i class="fa fa-gift" title="Send Gift"></i>
      <i class="far fa-comment-dots" title="Message"></i>
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
  justify-content: space-between;
  background-color: rgba(255, 255, 255, 0.03);
  border-radius: 4px;
  padding: 12px;
  color: #fff;
  border: 1px solid #333;
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
  flex-grow: 1;
}

.name {
  font-weight: bold;
  margin: 0;
}

.username,
.rating {
  font-size: 0.85rem;
  color: #bbb;
  margin: 2px 0;
}

.actions {
  display: flex;
  gap: 12px;
  align-items: center;
}

.actions i {
  font-size: 18px;
  transition: transform 0.2s;
  cursor: pointer;
}

.actions .fa-chess-board {
  color: #ffb74d;
}
.actions .fa-gift {
  color: #4fc3f7;
}
.actions .fa-comment-dots {
  color: #81c784;
}

.actions i:hover {
  transform: scale(1.2);
}
</style>
