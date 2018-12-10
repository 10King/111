<template>
  <div class="myheader">
    <div class="avatar">
      <img width="64" height="64" :src="seller.avatar"/>
    </div>
    <div class="content">
      <div class="title">
        <span></span>
        <span>{{seller.name}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props:["seller"],
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div.myheader{
  width: 100%;
  height: 134px;
  background-color: #ddd;
}
</style>
