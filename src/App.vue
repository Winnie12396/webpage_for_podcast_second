<template>
  <v-app>
    <div class="bar">
      <Toolbar/>
    </div>

    <router-view></router-view>
    
    

    
  </v-app>
</template>

<script>


import Toolbar from './components/Toolbar.vue'
export default {
  name: 'App',

  components: {
    Toolbar
  },

  data: () => ({
  
  }),
};
</script>

<style>

</style>

