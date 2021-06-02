<template>
<section>
  <v-app-bar app height="auto" >
    <div class="d-flex  flex-column">
      <div  class="d-flex justify-space-between ">
        <NuxtLink to="/">
          <img src="@/static/img/logo3.jpg" alt="">
        </NuxtLink>
        
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-lg-and-up"></v-app-bar-nav-icon>
      </div>
    
    
      
      <nav class="flex-column hidden-md-and-down">
        <v-tabs>
          <v-tab v-for="(link, i ) in links" :key="i" router :to="link.route">
            {{ link.text }}
          </v-tab>
        </v-tabs>
      </nav>
    </div>  

    
    
    
  </v-app-bar>
  
  <v-navigation-drawer
    v-model="drawer"
    app
    temporary
    
  >
    <v-system-bar></v-system-bar>
    <v-list nav dance>
      <v-list-item-group @click.stop="drawer = !drawer"  color="primary">
        <v-list-item  v-for="(link, i ) in links" :key="i" router :to="link.route" >
          <v-list-item-action >
            <v-icon v-text="link.icon"></v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="link.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>    
    </v-list>
  
  </v-navigation-drawer>
    
</section>  
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      links: [
        {icon:'mdi-home', text:'Главная', route: '/'},
        {icon:'mdi-home-group', text:'Проекты', route: '/main/projects'},
        {icon:'mdi-saw-blade', text:'Примеры работы', route: '/main/examples'},
        {icon:'mdi-account-star', text:'Отзывы клиентов', route: '/main/reviews'},
        {icon:'mdi-currency-rub', text:'Цены', route: '/main/other/prise'},
        {icon:'mdi-map-marker-radius', text:'Контакты', route: '/main/other/contacts'},
      ],
    }
  },

}
</script>

<style>

</style>