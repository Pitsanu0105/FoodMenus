<template>
  <div class="hello">
    <img v-bind:src="menus[index].img" style="width : 20%;" > <br>
    Name {{menus[index].name}} <br>
    Price {{menus[index].price}}
    <up-vote :up-vote="upVote" :index="index" :vote = "menus[index].vote"></up-vote>
  </div>
</template>

<script>
import UpVote from './UpVote'

export default {
  props: ['menus', 'upVote', 'index'],
  data () {
    return {
    }
  },
  components: {
    UpVote
  }
}
</script>
