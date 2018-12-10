<template>
  <div class="seller">
    {{seller}}
  </div>
</template>

<script>
export default {
  name: 'seller',
  props:["seller"],
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.seller{
}
</style>
