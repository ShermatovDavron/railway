<template>
    <header class="header">
      <AppNavbar :list="lists" :link = "link"/>
    </header>
</template>

<script>
import AppNavbar from '@/components/App-navbar/AppNavbar.vue'

export default {
    components:{
      AppNavbar,
    },
    data(){
      return{
        lists:[
            "Biletlar","Yangiliklar","Narxlar"
        ],
        link:"link"

      }
    }
  }
</script>

<style scoped>

</style>