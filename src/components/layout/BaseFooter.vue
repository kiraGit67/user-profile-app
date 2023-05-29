<template>
  <div class="columns">
    <div class="column"><slot name="subtitle-left"></slot></div>
    <div class="column"><slot name="subtitle-middle"></slot></div>
    <div class="column"><slot name="subtitle-right"></slot></div>
  </div>
</template>

<style scoped>
.columns {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
</style>
