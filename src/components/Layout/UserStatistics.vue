<template>
  <section class="user-statistics">
    <div class="ratings-grid">
      <div
        v-for="rating in ratings"
        :key="rating.label"
        class="rating-card"
        :class="rating.class"
        :title="rating.label"
      >
        <!-- Top Row -->
        <div class="top-row">
          <div class="left">
            <i :class="['icon', rating.icon, rating.class]"></i>
            <span class="label">{{ rating.label }}</span>
          </div>
          <div class="score">{{ rating.score }}</div>
        </div>

        <!-- Bottom Row -->
        <div class="bottom-row">
          <i class="fas fa-cog settings-icon" @click.stop="configure(rating.label)"></i>
          <button class="play-btn" @click.stop="play(rating.label)">Play</button>
        </div>
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
  methods: {
    play(mode) {
      console.log(`Starting ${mode} game...`);
    },
    configure(mode) {
      console.log(`Configure settings for ${mode}...`);
    },
  },
};
</script>

<style scoped>
.ratings-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 10px;
}

.rating-card {
  background-color: rgba(255, 255, 255, 0.03);
  padding: 1rem;
  border-radius: 4px;
  color: #a1a0b6;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: background-color 0.2s ease, transform 0.2s ease;
  box-shadow: inset 0 -6px 8px -6px transparent;
}

.rating-card:hover {
  background-color: rgba(255, 255, 255, 0.07);
  transform: translateY(-2px);
  cursor: pointer;
}

.rating-card.blitz {
  box-shadow: inset 0 -6px 10px -11px #facc15;
}

.rating-card.bullet {
  box-shadow: inset 0 -6px 10px -11px #60a5fa;
}

.rating-card.rapid {
  box-shadow: inset 0 -6px 10px -11px #34d399;
}

.rating-card.puzzles {
  box-shadow: inset 0 -10px 10px -11px #f472b6;
}

.top-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.left {
  display: flex;
  align-items: center;
  gap: 8px;
}

.icon {
  font-size: 1.2rem;
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
  font-size: 1rem;
  color: #ffffff;
}

.score {
  font-size: 1.05rem;
  font-weight: 600;
  color: #ffffff;
}

.bottom-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 1.2rem;
}

.settings-icon {
  font-size: 1rem;
  color: #9ca3af;
  cursor: pointer;
  transition: color 0.2s ease;
}

.settings-icon:hover {
  color: #f3f3f3;
}

.play-btn {
  background-color: #3b82f6;
  color: white;
  font-size: 0.75rem;
  padding: 6px 14px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.play-btn:hover {
  background-color: #2563eb;
}
</style>
