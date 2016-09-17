<template>
  <div id="app">
    <add-menu :add-menu = "addMenu"></add-menu>
    <food-menus :menus="menus" :up-vote="upVote"></food-menus>
  </div>
</template>

<script>
import AddMenu from './components/AddMenu'
import FoodMenus from './components/FoodMenus'

export default {
  data () {
    return {
      menus: [{
        img: 'http://food.mthai.com/app/uploads/2016/01/iStock_000017042355_Small.jpg',
        name: 'ข้าวมันไก่',
        price: 30,
        vote: 0
      }]
    }
  },
  components: {
    AddMenu,
    FoodMenus
  },
  methods: {
    upVote (index) {
      this.menus[index].vote++
    },
    addMenu (img, name, price) {
      var menu = {
        img: img,
        name: name,
        price: price,
        vote: 0
      }
      this.menus.push(menu)
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
