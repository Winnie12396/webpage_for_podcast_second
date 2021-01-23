<template>
  <v-container>

    <v-layout row justify-center ma-4>
      <v-flex text-center xs12 md4 xl3 pt-18 pb-8>
        <h1>所有單集</h1>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-space-around pb-8>
      <v-flex xs6 md4 xl3
        v-for="item in items"
        :key="item.id"
        pa-4
      >
        <v-card>
          <v-img
            class="align-end"
            :aspect-ratio="1/1"
            :src="item.pic"
          >
          </v-img>
          <v-card-title>{{ item.title }}</v-card-title>
          <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
          
          <v-bottom-sheet inset hide-overlay persistent>
            <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="primary"
              dark
              
              v-bind="attrs"
              v-on="on"
              @click="play(item.index)"
            >
              播放
            </v-btn>
            </template>
            <v-card tile v-show="playerOpened">
              <v-list>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title>{{ playingTitle }}</v-list-item-title>
                    <v-list-item-subtitle>{{ playingSubtitle }}</v-list-item-subtitle>
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
          <v-btn
            color="third"
            hover
            @click="openoverlay(item.index)"
          >
            單集簡介
          </v-btn>
        </v-card>

      </v-flex>
          
    </v-layout>
    <v-overlay      
      :value="overlay"
      :z-index="zIndex"
      color="black"
      :opacity="opacity"
    >
      
      <v-layout row wrap justify-center>
        <v-flex xs8 md4 xl4 mb-6>
          <div class="text-wrapper">{{ overlaytext }}</div>
        </v-flex> 
      </v-layout>
      <v-layout row wrap justify-center>
        <v-btn
          icon
          color="white"
          large
          @click="overlay = false"
        >

          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-layout>
      
    </v-overlay>
  </v-container>
</template>

<script>
  export default {
    name: 'Episodescomp',

    data: () => ({
      overlay: false,
      opacity: 0.7,
      overlaytext: "",
      zIndex: 5,
      isPlaying: false,
      playerOpened: false,
      playingTitle: "",
      playingSubtitle: "",
      items: [
        {
          id: 1,
          index: 0,
          title: "Ep.1 今天是生物藝術！",
          subtitle: "來聊一個未來食物~",
          pic: require('@/assets/cloud1.jpg'),
          text: "在今天的節目中，我們會介紹荷蘭食物設計師Chloé Rutzerveld的作品Edible Growth，這件作品有許多有趣之處，按下播放鍵一探究竟吧～\n節目分段：\n0:00~3:40  3D列印食物? & Edible Growth簡介\n4:00~7:35  做為一個食物設計師\n7:50~13:25  推測設計?可以吃嗎? & 作品理念介紹\n13:45 ~        食物+科技=不健康? 一起聽聽Chloé的想法吧",
        },
        {
          id: 2,
          index: 1,
          title: "Ep.2 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲~",
          pic: require('@/assets/cloud2.jpg'),
          text: "《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。\n這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。本集為變奏2。",
        },
        {
          id: 3,
          index: 2,
          title: "Ep.3 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲~",
          pic: require('@/assets/cloud3.jpg'),
          text: "《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。\n這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。本集為變奏4。",
        },
        {
          id: 4,
          index: 3,
          title: "Ep.4 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲~",
          pic: require('@/assets/cloud1.jpg'),
          text: "《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。\n這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。本集為變奏6。",
        },
        {
          id: 5,
          index: 4,
          title: "Ep.5 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲~",
          pic: require('@/assets/cloud2.jpg'),
          text: "《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。\n這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。本集為變奏12。",
        },
        {
          id: 6,
          index: 5,
          title: "Ep.6 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲~",
          pic: require('@/assets/cloud3.jpg'),
          text: "《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。\n這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。本集為變奏18。",
        },
      ],
      current: {},
      songs: [
        {
          title: "Ep.1 今天是生物藝術！來聊一個未來食物",
          src: require('@/assets/final.mp3')
        },
        {
          title: "Ep.2 今天是古典樂！來聽巴哈的郭德堡變奏曲",
          src: require('@/assets/BWV988-Variatio2.mp3')
        },
        {
          title: "Ep.3 今天是古典樂！來聽巴哈的郭德堡變奏曲",
          src: require('@/assets/BWV988-Variatio4.mp3')
        },
        {
          title: "Ep.4 今天是古典樂！來聽巴哈的郭德堡變奏曲",
          src: require('@/assets/BWV988-Variatio6.mp3')
        },
        {
          title: "Ep.5 今天是古典樂！來聽巴哈的郭德堡變奏曲",
          src: require('@/assets/BWV988-Variatio12.mp3')
        },
        {
          title: "Ep.6 今天是古典樂！來聽巴哈的郭德堡變奏曲",
          src: require('@/assets/BWV988-Variatio18.mp3')
        },
      ],
      player: new Audio()
    }),
    methods: {
      play (passindex) {
        this.current = this.songs[passindex];
        this.player.src = this.current.src;
        this.player.play();
        this.isPlaying = true;
        this.playerOpened = true;
        this.playingTitle = this.songs[passindex].title;
        this.playingSubtitle = this.songs[passindex].subtitle;
      },
      pause () {
        this.player.pause();
        this.isPlaying = false;
      },
      playerClose () {
        this.playerOpened = false;
        this.pause();
      },
      openoverlay (passindex) {
        this.overlay = !this.overlay;
        this.overlaytext = this.items[passindex].text;
      }
    },
    created () {
      
    }
  }
</script>
<style>
.text-wrapper {
  white-space: pre-wrap;
  text-align: left;
}
</style>


<!--
  <div class="justify-space-between">

      <v-img
        class="align-end"
        max-width="350"
        :aspect-ratio="1"
        src="@/assets/logo-fish.jpg"
      >
      </v-img>
      <v-card
        class="mx-auto"
        max-width="336"
        flat
      >
        <v-card-title><h4>天空裡的魚</h4></v-card-title>
        <v-card-subtitle>播客</v-card-subtitle>

        <v-card-text>
          Phasellus magna. Quisque rutrum. Nunc egestas, augue at pellentesque laoreet, felis eros vehicula leo, at malesuada velit leo quis pede. Aliquam lobortis. Quisque libero metus, condimentum nec, tempor a, commodo mollis, magna.

          In turpis. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. In turpis. Pellentesque dapibus hendrerit tortor. Ut varius tincidunt libero.
        </v-card-text>
      </v-card>
    </div>

-->

<!--
    <v-row
      no-gutters
      align="center"
      align-content="center"
      justify-space-around
    >
      <v-col
        v-for="item in items"
        :key="item.id"
        cols="4"
      >

        <v-card
          class="mx-auto"
          aspect-ratio="3/5"

        >
          <v-img
            class="align-end"
            :aspect-ratio="1/1"
            src="@/assets/logo.png"
          >
          </v-img>
          <v-card-title>{{ item.title }}</v-card-title>
          <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>

          <v-card-text>
            {{ item.text }}
          </v-card-text>
          <v-btn
            color="primary"
          >
            播放
          </v-btn>
        </v-card>
      </v-col>
    
    </v-row>
-->