<template>
  <v-container>
    <v-layout row justify-center ma-4>
      <v-flex text-center xs12 md4 xl3 pt-18 pb-8>
        <h1>所有單集</h1>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-space-around>
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

          <v-card-text>
            {{ item.text }}
          </v-card-text>
          <v-btn
            color="primary"
            hover
            @click="play(item.index)"
          >
            播放
          </v-btn>
          <v-btn
            color="success"
            hover
            @click="pause"
          >
            暫停
          </v-btn>
        </v-card>

      </v-flex>
          
    </v-layout>   
  </v-container>
</template>

<script>
  export default {
    name: 'Episodescomp',

    data: () => ({
      isPlaying: false,
      items: [
        {
          id: 1,
          index: 0,
          title: "Ep.1 今天是生物藝術！",
          subtitle: "來聊一個未來食物",
          pic: require('@/assets/cloud1.jpg'),
          text: "",
          src: ""
        },
        {
          id: 2,
          index: 1,
          title: "Ep.2 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲",
          pic: require('@/assets/cloud2.jpg'),
          text: "",
          src: ""
        },
        {
          id: 3,
          index: 2,
          title: "Ep.3 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲",
          pic: require('@/assets/cloud3.jpg'),
          text: "",
          src: ""
        },
        {
          id: 4,
          index: 3,
          title: "Ep.4 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲",
          pic: require('@/assets/cloud1.jpg'),
          text: "",
          src: ""
        },
        {
          id: 5,
          index: 4,
          title: "Ep.5 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲",
          pic: require('@/assets/cloud2.jpg'),
          text: "",
          src: ""
        },
        {
          id: 6,
          index: 5,
          title: "Ep.6 今天是古典樂！",
          subtitle: "來聽巴哈的郭德堡變奏曲",
          pic: require('@/assets/cloud3.jpg'),
          text: "",
          src: ""
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
      },
      pause () {
        this.player.pause();
        this.isPlaying = false;
      },
    },
    created () {
      
    }
  }
</script>

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