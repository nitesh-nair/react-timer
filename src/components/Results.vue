<template>
  <div class="results">
    <p>Reaction Time: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
      return {
          rank: null
      }
  },
  mounted() {
      if (this.score < 250) {
          this.rank = "Excellent Reflexes"
      } else if (this.score <400) {
          this.rank = "Good Reflexes"
      }else {
          this.rank = "Poor Reflexes"
      }
  }
};
</script>

<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>