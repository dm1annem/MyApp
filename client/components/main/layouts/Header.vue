<template>
  <nav>
    <v-app-bar app >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>
        <span>Каркас</span>
        <span>Центр</span>
      </v-app-bar-title>
    </v-app-bar>
    
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      />
    
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    }
  },

}
</script>

<style>

</style>