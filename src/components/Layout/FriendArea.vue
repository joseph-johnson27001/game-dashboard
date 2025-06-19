<template>
  <div class="friend-area">
    <p>Friends</p>
    <FriendCard />
  </div>
</template>

<script>
import FriendCard from "@/components/UI/FriendCard.vue";

export default {
  components: {
    FriendCard,
  },
};
</script>

<style scoped>
.friend-area {
  margin-top: 10px;
}
</style>
