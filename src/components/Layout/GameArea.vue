<template>
  <div class="game-area">
    <div class="card" v-for="(game, index) in games" :key="index">
      <ChessBoard :fen="game.fen" />
      <p class="description">{{ game.description }}</p>
    </div>
  </div>
</template>

<script>
import ChessBoard from "@/components/Boards/ChessBoard.vue";

export default {
  name: "GameArea",
  components: {
    ChessBoard,
  },
  data() {
    return {
      games: [
        {
          fen: "r1bqkbnr/pppp1ppp/2n5/4p3/2B1P3/5N2/PPPP1PPP/RNBQK2R",
          description: "Italian Game: Early Development",
        },
        {
          fen: "rnbqkbnr/pp1ppppp/8/2p5/4P3/5N2/PPPP1PPP/RNBQKB1R",
          description: "English Opening Transition",
        },
        {
          fen: "r1bqk2r/pppp1ppp/2n2n2/2b1p3/4P3/2NP1N2/PPP2PPP/R1BQKB1R",
          description: "Classical King's Indian Structure",
        },
        {
          fen: "r2q1rk1/ppp2ppp/2n2n2/3bp3/3P4/2N1PN2/PPQ2PPP/R1B2RK1",
          description: "Queen's Gambit Declined: Midgame",
        },
      ],
    };
  },
};
</script>

<style scoped>
.game-area {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 10px;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 10px;
}

.card {
  padding: 12px;
  width: 320px;
  border-radius: 8px;
  text-align: center;
}

.description {
  margin-top: 8px;
  font-weight: 600;
  color: #fefefe;
}
</style>
