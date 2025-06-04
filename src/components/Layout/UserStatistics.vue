<template>
  <section class="user-statistics">
    <div class="ratings-grid">
      <div
        v-for="rating in ratings"
        :key="rating.label"
        class="rating-card"
        :title="rating.label"
      >
        <i :class="['icon', rating.icon, rating.class]"></i>
        <div class="label">{{ rating.label }}</div>
        <div class="score">{{ rating.score }}</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "UserStatistics",
  data() {
    return {
      ratings: [
        {
          label: "Blitz",
          icon: "fas fa-bolt",
          score: 1420,
          class: "blitz",
        },
        {
          label: "Bullet",
          icon: "fas fa-stopwatch",
          score: 1290,
          class: "bullet",
        },
        {
          label: "Rapid",
          icon: "fas fa-hourglass-half",
          score: 1532,
          class: "rapid",
        },
        {
          label: "Puzzles",
          icon: "fas fa-puzzle-piece",
          score: 1675,
          class: "puzzles",
        },
      ],
    };
  },
};
</script>

<style scoped>
.ratings-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
  gap: 1rem;
}

.rating-card {
  background-color: rgba(255, 255, 255, 0.03);
  padding: 1rem;
  border-radius: 12px;
  text-align: center;
  color: #a1a0b6;
  transition: background-color 0.2s ease;
}

.rating-card:hover {
  background-color: rgba(255, 255, 255, 0.07);
}

.icon {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.blitz {
  color: #facc15;
}
.bullet {
  color: #60a5fa;
}
.rapid {
  color: #34d399;
}
.puzzles {
  color: #f472b6;
}

.label {
  font-size: 0.95rem;
  margin-bottom: 0.25rem;
}

.score {
  font-size: 1.1rem;
  font-weight: 600;
  color: #ffffff;
}
</style>
