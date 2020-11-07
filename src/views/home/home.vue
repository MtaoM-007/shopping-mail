<template>
  <div>

  </div>
</template>

<script>
  export default {
    name: "home",
    data(){
      return{
        banner:[],
        recommend:[]
      }
    },

    created(){
      let xml = new XMLHttpRequest();
      xml.open("get","http://192.168.1.:3000//home/multidata")
      xml.send();
      xml.onreadystatechange = ()=>{
        if(xml.readyState==4 && xml.status == 200){
          this.banner = JSON.parse(xml.response).data.banner.list
          this.recommend = JSON.parse(xml.response).data.recommend.list

        }
      }
    },
    mounted() {

    }
  }
</script>

<style scoped>

</style>