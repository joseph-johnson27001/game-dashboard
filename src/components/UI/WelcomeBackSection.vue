<template>
  <div class="welcome-back-section">
    <h1>Welcome Back, {{ name }}! <i class="fa-solid fa-chess-rook"></i></h1>
    <p>Good to see you back here. Fancy a game?</p>
  </div>
</template>

<script>
export default {
  name: "WelcomeBackSection",
  props: {
    name: {
      type: String,
      default: "Joanne"
    }
  },
  data() {
    return {};
  },
  methods: {}
};
</script>


<style scoped>
h1 {
  color: #ffffff;
  font-size: 1.8rem;
  font-weight: 500;
  margin-bottom: 0px;
  margin-top: 0px;
  padding-top: 5px;
  padding-bottom: 5px;
}

.fa-chess-rook {
  color: gold;
  margin-left: 4px;
  font-size: 1.6rem;
  vertical-align: middle;
}

p {
  color: #a1a0b6;
  padding-top: 0px;
  margin-top: 0px;
  font-weight: 600;
}

</style>