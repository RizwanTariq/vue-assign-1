<template>
  <Header :list="itemList" :item="clickedItem" :handleClick="handleClick" />
  <Main :handleSubmit="handleSubmit" :item="clickedItem" />
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
  data() {
    return {
      itemList: [],
      clickedItem: '',
    }
  },
  methods: {
    handleSubmit(item) {
      this.itemList = [...this.itemList, item]
    },
    handleClick(item) {
      this.clickedItem = item
    },
  },
}
</script>
