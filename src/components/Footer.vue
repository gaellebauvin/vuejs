<template>
  <div class="footer">
    <ul>
      <li v-for="link in links" :key="link.id">{{link.title}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Footer',
  data() {
    return {
      links: [
        {id: 1, title: 'Lien 1'},
        {id: 2, title: 'Lien 2'},
        {id: 3, title: 'Lien 3'}
      ]
    }
  },
}
</script>

<style lang="scss">
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