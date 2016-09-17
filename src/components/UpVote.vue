<template>
  <div class="hello">
    <button @click="upVote(index)"> vote {{vote}}</button>
  </div>
</template>

<script>
export default {
  props: ['upVote', 'index', 'vote']
}

</script>
