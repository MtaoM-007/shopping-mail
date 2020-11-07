<template>
  <div class="tab-bar-item" @click="cclick" :style="color  changeColor">
    <slot name="icon"></slot>
    <slot name="text"></slot>
  </div>
</template>

<script>
  export default {
    name: "TabBaItem",
    props:{
      path:String,
      col:{
        type:String,
        default:"red"
      }
    },
    computed:{
      isActive(){
        return this.$route.path.indexOf(this.path) !=-1 ? true :false
      }
    },
    methods:{
      cclick(){
        this.$router.push(this.path)
      }
    }
  }
</script>

<style scoped>
  .tab-bar-item{
    margin-top: 5px;
    flex: 1;
  }
  .active{
    color: red;
  }
</style>