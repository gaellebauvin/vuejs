<template>
  <div class="header">
  <img alt="Vue logo" src="../assets/logo.png">
  <div class="menu">
    <ul>
      <li v-for="menu in menus" :key="menu.id">{{menu.title}}</li>
    </ul>
  </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      menus: [
        {id: 1, title: 'Menu 1'},
        {id: 2, title: 'Menu 2'},
        {id: 3, title: 'Menu 3'}
      ]
    }
  }
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
</style>