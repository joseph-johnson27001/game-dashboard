<template>
  <p>Game History</p>
  <GameHistoryTable />
</template>

<script>
import GameHistoryTable from "@/components/Table/GameHistoryTable.vue";
export default {
  name: "GameHistory",
  components: {
    GameHistoryTable,
  },
};
</script>
