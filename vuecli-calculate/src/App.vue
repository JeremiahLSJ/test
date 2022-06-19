<template>
  <div id="app">
    <ul>
      <li v-for="(item, index) in arr" :key="item">
        <span>{{ item }}</span>
        <button @click="del(index)">删除</button>
      </li>
    </ul>
    <button @click="add">添加</button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      arr:[1,5,3]
    }
  },
  methods: {
    add() {
      this.arr.push((Math.random()*10).toFixed(0))
    },
    del(index) {
      this.arr.splice(index, 1)
    }
  }
}
</script>

<style>

</style>
