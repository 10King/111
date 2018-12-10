<template>
  <div id="app">
    <myheader :seller="seller"></myheader>
    <div class="tab">
      <router-link to="/goods">商品</router-link>
      <router-link to="/ratings">评论</router-link>
      <router-link to="/seller">卖家</router-link>
    </div>
    <router-view :goods="goods" :ratings="ratings" :seller="seller"></router-view>
  </div>
</template>

<script>
import myheader from '@/components/myheader/myheader'
import axios from 'axios'
export default {
  name: 'App',
  components:{
    myheader
  },
  data(){
    return{
      seller:{},
      goods:[],
      ratings:[]
    }
  },
  created() {
    this.getData()
  },
  methods:{
    getData(){
      // console.log("getData")
      let url= 'http://localhost:81/getData'
      axios.get(url).then(r=>{
       console.log('r:', r)
       this.seller=r.data.seller
       this.goods=r.data.goods
       this.ratings=r.data.ratings
      }, err=>{
        console.log('err:', err)
      })
    }
  }
}
</script>

<style>
div#app div.tab{
  display: flex;
  height: 40px;
  line-height: 40px;
}
div#app div.tab a{
  text-align: center;
  flex: 1;
  color: #666;
  text-decoration: none;
  border-bottom: 1px solid transparent;
}
/*选中样式*/
div#app div.tab a.myAcitve{
  color: red;
  border-bottom: 1px solid red;
}
</style>
