<template>
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
      <Episodes/>
    
    </v-content>
    
    

    
  </v-app>
</template>

<script>

import Intro from './components/Intro.vue'
import Latest from './components/Latest.vue'
import Episodes from './components/Episodes.vue'
export default {
  name: 'App',

  components: {
    Intro,
    Latest,
    Episodes
  },

  data: () => ({
  
  }),
};
</script>

<style>

</style>

