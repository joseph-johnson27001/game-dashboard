<template>
  <section class="game-area">
    <div class="games-grid">
      <div
        v-for="game in games"
        :key="game.label"
        class="game-card"
        :class="game.class"
        :title="game.label"
      >
        <!-- Top Row -->
        <div class="top-row">
          <div class="left">
            <i :class="['icon', game.icon, game.class]"></i>
            <span class="label">{{ game.label }}</span>
          </div>
          <div class="score">{{ game.score }}</div>
        </div>

        <!-- Bottom Row -->
        <div class="bottom-row">
          <div class="dropdown-wrapper">
            <select
              class="setup-select"
              v-model="game.selected"
              @change="configure(game)"
            >
              <option
                v-for="option in getSetupOptions(game.label)"
                :key="option"
                :value="option"
              >
                {{ option }}
              </option>
            </select>
            <span class="dropdown-icon">▼</span>
          </div>
          <button class="play-btn" @click.stop="play(game)">Play</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "GameArea",
  data() {
    return {
      games: [
        {
          label: "Blitz",
          icon: "fas fa-bolt",
          score: 1420,
          class: "blitz",
          selected: "3 | 0",
        },
        {
          label: "Bullet",
          icon: "fas fa-stopwatch",
          score: 1290,
          class: "bullet",
          selected: "1 | 0",
        },
        {
          label: "Rapid",
          icon: "fas fa-hourglass-half",
          score: 1532,
          class: "rapid",
          selected: "10 | 0",
        },
        {
          label: "Puzzles",
          icon: "fas fa-puzzle-piece",
          score: 1675,
          class: "puzzles",
          selected: "Daily Puzzle",
        },
      ],
    };
  },
  methods: {
    getSetupOptions(label) {
      switch (label) {
        case "Bullet":
          return ["1 | 0", "1 | 1", "2 | 1"];
        case "Blitz":
          return ["3 | 0", "3 | 2", "5 | 0", "5 | 3"];
        case "Rapid":
          return ["10 | 0", "10 | 5", "15 | 10"];
        case "Puzzles":
          return ["Daily Puzzle", "Timed", "Survival"];
        default:
          return [];
      }
    },
    configure(game) {
      console.log(`Setup selected for ${game.label}: ${game.selected}`);
    },
    play(game) {
      const mode = game.label;
      const setup = game.selected || "default";
      console.log(`Playing ${mode} with setup: ${setup}`);
    },
  },
};
</script>

<style scoped>
.games-grid {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 10px;
}

.game-card {
  background-color: rgba(255, 255, 255, 0.03);
  padding: 1rem;
  border-radius: 4px;
  border-bottom-right-radius: 0px;
  border-bottom-left-radius: 0px;
  color: #a1a0b6;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: background-color 0.2s ease, transform 0.2s ease;
  box-shadow: inset 0 -6px 8px -6px transparent;
}

.game-card:hover {
  cursor: pointer;
}

.game-card.blitz {
  box-shadow: inset 0 -6px 10px -11px #facc15;
}
.game-card.bullet {
  box-shadow: inset 0 -6px 10px -11px #60a5fa;
}
.game-card.rapid {
  box-shadow: inset 0 -6px 10px -11px #34d399;
}
.game-card.puzzles {
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
  align-items: flex-end;
  margin-top: 1.2rem;
}

.dropdown-wrapper {
  position: relative;
  display: inline-block;
}

.setup-select {
  background-color: #3b82f6;
  color: white;
  font-size: 0.75rem;
  padding: 6px 24px 6px 10px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  appearance: none;
  outline: none;
  transition: background-color 0.2s ease;
  width: auto;
  max-width: 100%;
}

.setup-select:hover {
  background-color: #2563eb;
}

.dropdown-icon {
  position: absolute;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  color: white;
  font-size: 0.6rem;
  pointer-events: none;
}

.play-btn {
  background-color: #6366f1;
  color: white;
  font-size: 0.85rem;
  padding: 6px 14px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.play-btn:hover {
  background-color: #4f46e5;
}

@media (min-width: 640px) {
  .games-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .games-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
