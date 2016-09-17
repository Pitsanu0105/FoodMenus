<template>
  <div class="hello">
    <div v-for = "menu in menus | orderBy 'vote' -1">
      <food-menu :menus="menus" :up-vote="upVote" :index ="$index"><food-menu>
    </div>
  </div>
</template>

<script>
import FoodMenu from './FoodMenu'

export default {
  props: ['menus', 'upVote'],
  data () {
    return {
    }
  },
  components: {
    FoodMenu
  }
}
</script>
