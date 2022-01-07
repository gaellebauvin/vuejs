<template>
  <div id="app">
    <div class="header">
      <img alt="Vue logo" src="./assets/logo.png">
      <div class="menu">
        <ul>
          <li v-for="menu in menus" :key="menu.id">{{menu.title}}</li>
        </ul>
      </div>
    </div>
    <div class="main">
      <h1 v-text="titleContent" class="title"></h1>
      <p>La valeur de la variable result est : {{result}}</p>
      <p v-if="result === 0">Le paragraphe s'affiche car cette variable est égale à 0</p>
      <div class="content-actions">
        <button @click="increment">Incrément</button>
        <button @click="reset">Reset</button>
      </div>
    </div>

    <div class="footer">
      <ul>
        <li v-for="link in links" :key="link.id">{{link.title}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      titleContent: 'Hello le monde',
      result: 0,
      menus: [
        {id: 1, title: 'Menu 1'},
        {id: 2, title: 'Menu 2'},
        {id: 3, title: 'Menu 3'}
      ],
      links: [
        {id: 1, title: 'Lien 1'},
        {id: 2, title: 'Lien 2'},
        {id: 3, title: 'Lien 3'}
      ]
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
  .header {
    display: flex;
    justify-content: space-between;
    margin: 2% 5%;

    img {
      width: 5%;
    }

    .menu {
      display: flex;
      justify-content: end;
      width: 50%;
      ul {
        display: flex;
        width: 100%;
        justify-content: end;
        li {
          list-style: none;
          margin: 0 7%;
        }
      }
    }
  }

  .main {
    min-height: calc(100vh - 200px);
    text-align: center;
    .title {
      color : blue;
    }
    button {
      margin: 0 10px;
    }
  }

  .footer {
    padding: 20px 40px;
    ul {
      list-style: none;
      padding: 0;
      margin: 0 -10px;
      display: flex;
      align-items: center;
      justify-content: center;
      li {
        padding: 0 10px;
      }
    }
  }
</style>