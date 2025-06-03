<template>
  <div class="welcome-back-section">
    <h1>Welcome Back, {{ name }}!</h1>
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
    font-size: 2rem;
    margin-bottom: 0px;
    padding-bottom: 5px;
}

p {
    color: #a1a0b6;
    padding-top: 5px;
    margin-top: 0px;
}

</style>