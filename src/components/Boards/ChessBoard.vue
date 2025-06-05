<template>
  <div class="chessboard-wrapper">
    <TheChessboard
      :position="fen"
      :boardWidth="boardSize"
      :boardHeight="boardSize"
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
      boardSize: "300px",
    };
  },
};
</script>

<style scoped>
.chessboard-wrapper {
  width: 100%;
  aspect-ratio: 1 / 1;
}

/* BELOW IS COMING FROM THE SVG. IT ORIGINALLY IS SET TO 90VH FOR SOME REASON */
.main-wrap {
  width: 100%;
}
</style>
