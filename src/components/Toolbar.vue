<template>
  <v-container>
    
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
        
        <v-toolbar-items class="hidden-xs-only">
        
          <v-btn text href="/home">主頁</v-btn>
          <v-btn text href="/about">關於</v-btn>
          <v-btn text href="/episodes">所有單集</v-btn>
          <v-btn text href="/articles">文章</v-btn>
        
        </v-toolbar-items>
        <div class="hidden-sm-and-up">
          <v-menu offset-y>
            <template v-slot:activator="{ on, attrs }">
              <v-app-bar-nav-icon v-bind="attrs" v-on="on"></v-app-bar-nav-icon>
            </template>
            <v-list>
              <v-list-item>
                <v-btn text href="/home">主頁</v-btn>
                <v-btn text href="/about">關於</v-btn>
                <v-btn text href="/episodes">所有單集</v-btn>
                <v-btn text href="/articles">文章</v-btn>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>
        
      </v-toolbar>
    
    </v-app-bar>

  </v-container>
</template>

<script>
  export default {
    name: 'Toolbar',

    data: () => ({
    }),
  }
</script>

<style>



</style>

