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
          fen: "rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR",
          description: "Match Review",
        },
        {
          fen: "r1bqkbnr/pppppppp/2n5/8/4P3/5N2/PPPP1PPP/RNBQKB1R",
          description: "Play Computer",
        },
        {
          fen: "r1bqkbnr/pppppppp/2n5/8/4P3/8/PPPP1PPP/RNBQKBNR",
          description: "Lesson: Basic Opening",
        },
      ],
    };
  },
};
</script>

<style scoped>
.game-area {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

.card {
  border: 1px solid #ccc;
  padding: 12px;
  width: 320px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  text-align: center;
}

.description {
  margin-top: 8px;
  font-weight: 600;
  color: #333;
}
</style>
