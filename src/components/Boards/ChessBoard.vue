<template>
  <div class="chessboard-wrapper">
    <TheChessboard
      :boardWidth="boardSize"
      :boardHeight="boardSize"
      @boardCreated="onBoardCreated"
    />
  </div>
</template>

<script>
import { TheChessboard } from "vue3-chessboard";
import "vue3-chessboard/style.css";

export default {
  name: "ChessBoard",
  components: {
    TheChessboard,
  },
  props: {
    fen: { type: String, required: true },
  },
  data() {
    return {
      boardSize: 300,
      boardAPI: null,
    };
  },
  methods: {
    onBoardCreated(api) {
      this.boardAPI = api;
      this.boardAPI.board.set({ fen: this.fen });
    },
  },
};
</script>

<style scoped>
.chessboard-wrapper {
  width: 100%;
}

/* BELOW IS COMING FROM THE SVG. IT ORIGINALLY IS SET TO 90VH FOR SOME REASON */
.main-wrap {
  width: 100%;
}
</style>
