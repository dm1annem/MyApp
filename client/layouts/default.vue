<template>
<v-app>
  <my-header/>

  <v-main >
    <v-container >
      <Nuxt />
    </v-container>
  </v-main>

  <my-footer/>
</v-app>
</template>

<script>
import MyHeader from '@/components/main/layouts/Header.vue'
import MyFooter from '@/components/main/layouts/Footer'
export default {
  components:{
        MyHeader,
        MyFooter,
  },
  data () {
    return {
      
      
    }
  }
}
</script>
