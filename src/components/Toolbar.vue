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
          <v-toolbar-items>
            <v-btn text href="/home">主頁</v-btn>
            <v-btn text href="/about">關於</v-btn>
            <v-btn text href="/episodes">所有單集</v-btn>
            <v-btn text>文章</v-btn>
          </v-toolbar-items>
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

