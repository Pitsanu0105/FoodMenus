<template>
  <div class="hello">
    img : <input v-model = "img"> <br>
    name : <input v-model = "name"> <br>
    Price : <input v-model = "price"> <br>
    <button @click="addMenu(img,name,price)">Add</button>
  </div>
</template>

<script>
export default {
  props: ['addMenu'],
  data () {
    return {
      img: '',
      name: '',
      price: ''
    }
  }
}
</script>
