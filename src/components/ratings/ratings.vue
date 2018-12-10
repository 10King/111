<template>
  <div class="ratings">
    {{ratings}}
    <br/>
    <br/>
    <br/>
    <br/>
    {{seller}}
  </div>
</template>

<script>
export default {
  name: 'ratings',
  props:["ratings","seller"],
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.ratings{
}
</style>
