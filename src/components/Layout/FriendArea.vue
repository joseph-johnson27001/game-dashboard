<template>
  <div class="friend-area">
    <p class="title">Online Friends</p>
    <div class="friend-list">
      <FriendCard
        v-for="(friend, index) in friends"
        :key="index"
        :name="friend.name"
        :username="friend.username"
        :rating="friend.rating"
        :avatar="friend.avatar"
      />
    </div>
  </div>
</template>

<script>
import FriendCard from "@/components/UI/FriendCard.vue";

export default {
  components: {
    FriendCard,
  },
  data() {
    return {
      friends: [
        {
          name: "Alice Johnson",
          username: "chessqueen28",
          rating: 1720,
          avatar: "https://randomuser.me/api/portraits/women/22.jpg",
        },
        {
          name: "Marcus Lee",
          username: "rookwarrior",
          rating: 1855,
          avatar: "https://randomuser.me/api/portraits/men/52.jpg",
        },
        {
          name: "Sophia Lin",
          username: "knightstorm",
          rating: 1990,
          avatar: "https://randomuser.me/api/portraits/women/44.jpg",
        },
        {
          name: "Daniel Rivera",
          username: "bishopblitz",
          rating: 1625,
          avatar: "https://randomuser.me/api/portraits/men/33.jpg",
        },
        {
          name: "Lily Thompson",
          username: "queenforker",
          rating: 2103,
          avatar: "https://randomuser.me/api/portraits/women/12.jpg",
        },
        {
          name: "Ethan Brooks",
          username: "endgameking",
          rating: 1940,
          avatar: "https://randomuser.me/api/portraits/men/45.jpg",
        },
        {
          name: "Chloe Martin",
          username: "checkmatechloe",
          rating: 1888,
          avatar: "https://randomuser.me/api/portraits/women/37.jpg",
        },
        {
          name: "Noah Bennett",
          username: "tacticalnoah",
          rating: 1764,
          avatar: "https://randomuser.me/api/portraits/men/27.jpg",
        },
      ],
    };
  },
};
</script>

<style scoped>
.friend-area {
  margin-top: 10px;
}

.friend-list {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
}

@media (max-width: 1250px) {
  .friend-list {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 700px) {
  .friend-list {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
