<template>
  <p>Learning & Tactics</p>
  <div class="learning-area">
    <div class="card" v-for="(game, index) in games" :key="index">
      <ChessBoard :fen="game.fen" />
      <p class="description">{{ game.description }}</p>
    </div>
  </div>
</template>

<script>
import ChessBoard from "@/components/Boards/ChessBoard.vue";

export default {
  name: "LearningArea",
  components: {
    ChessBoard,
  },
  data() {
    return {
      games: [
        {
          fen: "r1bqkbnr/pppp1ppp/2n5/2b1p3/2B1P3/5N2/PPPP1PPP/RNBQK2R w KQkq - 2 4",
          description: "Italian Game: Early Development",
        },
        {
          fen: "rnbqkbnr/pppppppp/8/8/2P5/8/PP1PPPPP/RNBQKBNR b KQkq c3 0 1",
          description: "English Opening Transition",
        },
        {
          fen: "rnbq1rk1/ppp1ppbp/3p1np1/4p3/2PP4/2N1PN2/PP2BPPP/R1BQ1RK1 w - - 0 7",
          description: "Classical King's Indian Structure",
        },
        {
          fen: "rnbq1rk1/ppp1bppp/4pn2/2p1B3/2P5/2N1P3/PP3PPP/R2QKBNR w KQ - 0 6",
          description: "Queen's Gambit Declined: Midgame",
        },
      ],
    };
  },
};
</script>

<style scoped>
.learning-area {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 10px;
  justify-content: center;
  margin-top: 10px;
}

.card {
  border-radius: 8px;
  text-align: center;
}

.description {
  font-family: "Assistant", sans-serif;
  margin-top: 8px;
  font-weight: 400;
  color: #fefefe;
  margin-bottom: 0px;
}

@media (min-width: 640px) {
  .learning-area {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .learning-area {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
