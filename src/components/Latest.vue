<template>
  <v-container>

    <v-layout row justify-center ma-4>
      <v-flex xs12 md4 xl3 pt-12 class="thisparttitle">
        <h2>最新單集</h2>
      </v-flex>
    </v-layout>
    <v-layout row justify-center ma-4>

      <v-flex xs12 sm6 md4 xl3 pt-12 pb-50>
        <v-card
          class="mx-auto"
        >
          <v-img
            class="align-end"
            :aspect-ratio="1/1"
            src="@/assets/ep6.jpg"
            max-height="336"
          >
          </v-img>
          <v-card-title>Ep.6 今天是古典樂！</v-card-title>
          <v-card-subtitle>來聽巴哈的郭德堡變奏曲</v-card-subtitle>

          <v-card-text>
            《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。

            這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。
          </v-card-text>
          <v-bottom-sheet inset hide-overlay persistent>
            <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="primary"
              dark
              v-bind="attrs"
              v-on="on"
              @click="play"
            >
              播放
            </v-btn>
            </template>
            <v-card tile v-show="playerOpened">
              <v-list>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title>Ep.6 今天是古典樂！</v-list-item-title>
                    <v-list-item-subtitle>來聽巴哈的郭德堡變奏曲</v-list-item-subtitle>
                  </v-list-item-content>

                  <v-spacer></v-spacer>

                  <v-list-item-icon :class="{ 'mx-5': $vuetify.breakpoint.mdAndUp }">
                    <v-btn icon>
                      <v-icon v-if="isPlaying" @click="pause">mdi-pause</v-icon>
                      <v-icon v-else>mdi-play</v-icon>
                    </v-btn>
                  </v-list-item-icon>

                  <v-list-item-icon
                    class="ml-0"
                    :class="{ 'mr-3': $vuetify.breakpoint.mdAndUp }"
                  >
                    <v-btn icon @click="playerClose">
                      <v-icon>mdi-close</v-icon>
                    </v-btn>
                  </v-list-item-icon>
                </v-list-item>
              </v-list>
            </v-card>
          </v-bottom-sheet>  
        </v-card>
        <v-spacer></v-spacer>
      </v-flex>
      
      
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    name: 'Latest',

    data: () => ({
      player: new Audio(),
      isPlaying: false,
      playerOpened: false,
    }),
    methods: {
      play () {
        this.player.src = require('@/assets/BWV988-Variatio18.mp3');
        this.player.play();
        this.isPlaying = true;
        this.playerOpened = true;

      },
      pause () {
        this.player.pause();
        this.isPlaying = false;
      },
      playerClose () {
        this.playerOpened = false;
        this.pause();
      },
    }
  }
</script>

<style>
.thisparttitle {
  text-align: center;
}


</style>

