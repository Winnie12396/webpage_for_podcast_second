<template>
  <v-app>
    <div class="bar">
      <Toolbar/>
    </div>

    <v-content>
      <Intro/>
      <Latest/>
      <Episodes/>
    
    </v-content>
    
    

    
  </v-app>
</template>

<script>

import Intro from './components/Intro.vue'
import Latest from './components/Latest.vue'
import Episodes from './components/Episodes.vue'
import Toolbar from './components/Toolbar.vue'
export default {
  name: 'App',

  components: {
    Intro,
    Latest,
    Episodes,
    Toolbar
  },

  data: () => ({
  
  }),
};
</script>

<style>

</style>

