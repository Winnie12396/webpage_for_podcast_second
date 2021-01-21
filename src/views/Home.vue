<template>
  <div class="home">
    <v-app>
      <div class="bar">
        <v-app-bar
          app
          color="white"
          flat
        >
          <v-toolbar
            flat
          >

            <v-toolbar-title><h4>天空裡的魚 Fish in the Sky</h4></v-toolbar-title>

            <v-spacer></v-spacer>
            <v-toolbar-items>
              <v-btn text href="/home">主頁</v-btn>
              <v-btn text href="/about">關於</v-btn>
              <v-btn text>所有單集</v-btn>
              <v-btn text>文章</v-btn>
            </v-toolbar-items>
          </v-toolbar>
        </v-app-bar>

      </div>

      <v-content>
        <Intro/>
        <Latest/>
      
      </v-content>
      
      

      
    </v-app>
  </div>
</template>

<script>

import Intro from '@/components/Intro.vue'
import Latest from '@/components/Latest.vue'
export default {
  name: 'Home',

  components: {
    Intro,
    Latest
  },

  data: () => ({
  
  }),
};
</script>
