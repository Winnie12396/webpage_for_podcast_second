<template>
  <div class="home">
    <v-app>
      

      <v-content>
        <Intro/>
        <Latest/>
        <Episodes-component/>
      
      </v-content>
      
      

      
    </v-app>
  </div>
</template>

<script>

import Intro from '../components/Intro.vue'
import Latest from '../components/Latest.vue'
import Episodescomp from '../components/Episodescomp.vue'
import Toolbar from '../components/Toolbar.vue'
export default {
  name: 'Home',

  components: {
    Intro,
    Latest,
    Episodescomp,
    Toolbar
  },

  data: () => ({
  
  }),
};
</script>
