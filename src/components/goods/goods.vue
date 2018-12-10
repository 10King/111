<template>
  <div class="goods">
    {{goods}}
    {{goods.length}}
  </div>
</template>

<script>
export default {
  name: 'goods',
  // props:{
  //   goods:{
  //     type:Array,
  //     default(){
  //       return []
  //     }
  //   }
  // },
  props:["goods"],
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.goods{
}
</style>
