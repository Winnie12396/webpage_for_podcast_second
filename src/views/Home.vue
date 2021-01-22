<template>
  <div class="home">
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
  </div>
</template>

<script>

import Intro from '../components/Intro.vue'
import Latest from '../components/Latest.vue'
import Episodes from '../components/Episodes.vue'
import Toolbar from '../components/Toolbar.vue'
export default {
  name: 'Home',

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
