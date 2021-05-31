<template>
<section>
  <v-app-bar app >
    <NuxtLink to="/">
      <img src="@/static/img/logo3.jpg" alt="">
    </NuxtLink>

    <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-lg-and-up"></v-app-bar-nav-icon>
    
  </v-app-bar>
  
  <v-navigation-drawer
    v-model="drawer"
    absolute
    temporary
    >
    <v-list>
      <v-list-tile v-for="link in links" :key="link.text">
        <v-list-tile-action>
          <v-icon> {{ link.icon }} </v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>
            {{ link.text }}
          </v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
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
        {icon:'mdi-home', text:'Главная страница', route: '/'},
        {icon:'mdi-home', text:'Проекты', route: '/'},
      ],
    }
  },

}
</script>

<style>

</style>