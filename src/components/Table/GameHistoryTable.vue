<template>
  <div class="game-history-table">
    <table>
      <thead>
        <tr>
          <th>Type</th>
          <th>White</th>
          <th>Black</th>
          <th>Result</th>
          <th>Accuracy</th>
          <th>Moves</th>
          <th>Date</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(game, index) in games" :key="index">
          <td>{{ game.type }}</td>
          <td>{{ game.white }}</td>
          <td>{{ game.black }}</td>
          <td>{{ game.result }}</td>
          <td>{{ game.accuracy }}%</td>
          <td>{{ game.moves }}</td>
          <td>{{ formatDate(game.date) }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "GameHistoryTable",
  data() {
    return {
      games: [
        {
          type: "Blitz",
          white: "ChessMaster12",
          black: "QuickMate9",
          result: "1-0",
          accuracy: 89,
          moves: 42,
          date: "2025-06-10T15:30:00Z",
        },
        {
          type: "Bullet",
          white: "FastBishop",
          black: "KnightStorm",
          result: "0-1",
          accuracy: 75,
          moves: 28,
          date: "2025-06-08T20:15:00Z",
        },
        {
          type: "Rapid",
          white: "EndGameKing",
          black: "PawnPower",
          result: "½-½",
          accuracy: 92,
          moves: 65,
          date: "2025-05-30T18:00:00Z",
        },
        {
          type: "Classical",
          white: "DeepThinker",
          black: "BlunderTrap",
          result: "1-0",
          accuracy: 97,
          moves: 78,
          date: "2025-04-25T14:45:00Z",
        },
      ],
    };
  },
  methods: {
    formatDate(dateStr) {
      const date = new Date(dateStr);
      return date.toLocaleDateString("en-US", {
        year: "numeric",
        month: "short",
        day: "numeric",
      });
    },
  },
};
</script>

<style scoped>
.game-history-table {
  padding: 10px;
  background-color: #1e1e2f;
  border-radius: 8px;
  overflow-x: scroll;
  -ms-overflow-style: none;
}

.game-history-table::-webkit-scrollbar {
  display: none;
}

.title {
  margin-bottom: 16px;
  font-size: 24px;
  color: #f4f4f4;
}

table {
  width: 100%;
  border-collapse: collapse;
  color: #f0f0f0;
  font-size: 14px;
}

thead {
  background-color: #2a2a3d;
}

th,
td {
  padding: 12px 16px;
  text-align: left;
}

tbody tr:nth-child(odd) {
  background-color: #292940;
}

tbody tr:nth-child(even) {
  background-color: #222236;
}

th {
  font-weight: 600;
  color: #ffffff;
}

tbody tr:hover {
  background-color: #3a3a4d;
  cursor: pointer;
}

td {
  color: #dddddd;
}

@media (max-width: 768px) {
  .title {
    font-size: 20px;
  }

  th,
  td {
    padding: 8px 10px;
    font-size: 12px;
  }
}
</style>
