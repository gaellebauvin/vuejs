<template>
  <div class="main">
    <h1 v-text="titleContent" class="title"></h1>
    <p>La valeur de la variable result est : {{result}}</p>
    <p v-if="result === 0">Le paragraphe s'affiche car cette variable est égale à 0</p>
    <div class="content-actions">
      <button @click="increment">Incrément</button>
      <button @click="reset">Reset</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {
      titleContent: 'Hello le monde',
      result: 0,
    }
  },
  methods: {
    reset() {
      this.result = 0
    },
    increment() {
      this.result++
    }
  },
}
</script>

<style lang="scss">
.main {
  min-height: calc(100vh - 200px);
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
    .title {
      color : blue;
    }
    button {
      margin: 0 10px;
    }
}
</style>