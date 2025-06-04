<template>
  <div class="welcome-back-section">
    <h1>Welcome Back, {{ name }}! <i class="fa-solid fa-chess-rook"></i></h1>
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
  color: #f3f3f3;
  font-size: 1.4rem;
  font-weight: 500;
  margin-bottom: 0px;
  margin-top: 0px;
  padding-top: 0px;
  padding-bottom: 10px;
  display: flex;
  align-items: center;
}

.fa-chess-rook {
  color: gold;
  margin-left: 6px;
  font-size: 1.4rem;
  vertical-align: middle;
}

p {
  padding-top: 0px;
  margin-top: 0px;
  font-weight: 500;
}

</style>