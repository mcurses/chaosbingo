<template>
  <div class="bingo-grid">
    <bingo-cell v-for="cell in grid" :key="cell.id" :cell="cell"></bingo-cell>
  </div>
</template>

<script>
import BingoCell from './BingoCell.vue';

export default {
  components: { BingoCell },
  props: ['grid']
};
</script>
