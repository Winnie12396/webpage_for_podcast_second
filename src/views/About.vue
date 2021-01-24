<template>
  <v-content class="about">

    <v-layout row wrap justify-center pt-12>
      <v-flex xs12 md8 px-10 mb-10>
        <body-1>
          <p>天空裡的魚，這個節目的起源，是一個19歲大學女生，在一次期末作業之中突發奇想，也許可以來試試看做podcast這件事。</p>
          <p>這個作業是生物藝術概論課的期末作業，要做形式不拘的藝術普及，介紹生物藝術的作品；我的成品就是第一集的內容。</p>
          <p>不過在做的過程中，想到可以分享的主題越來越多，</p>
          <p>於是這個節目就有了在期末之後繼續做下去的可能。</p>
          <p>目前希望一個月一到兩集，寒暑假會多一點。</p>
          <p>期待與你相見！</p>
          <p>目前在<a href="https://open.firstory.me/user/fishinthesky">Firstory</a>、<a href="https://podcast.kkbox.com/channel/P_Rw-Q1b7808oGoPbC">KKbox</a>、<a href="https://open.spotify.com/show/4cMfhxhkGo6a0xaYfakCeG">Spotify</a>、Apple Podcasts跟PocketCasts皆可收聽喔</p>
          <p>有任何想聊的可以私訊 IG @fishinthesky1212 或寄信給我：fishinthesky1212@gmail.com</p>
        </body-1>

      </v-flex>
      
    </v-layout>
    <v-divider></v-divider>
    <v-layout row wrap justify-center pt-12 pb-50>
      <v-flex xs12 md8 px-10 pb-10>
        <div class="concept"><h3>網頁設計理念概述</h3></div>
        <body-1>
          <p>這份期末作業，我原本是想把期中啟發自gamified design的簡單網頁再做擴充，但畫設計圖的時候覺得沒辦法兼顧內容、理念跟美感，響應式的技術問題也不知道怎麼解決，就先擱置。</p>
          <p>另一方面，我發現我期中一直在找新的設計想法，所以期末還是回過頭來把技術的東西研究研究好了。</p>
          <p>剛好生物藝術概論的期末做了以前沒有做過的東西，我就想說來幫我的節目寫個網頁，而且要讓這個網頁有實際功能，可以播出音訊。</p>
          <p>這個網頁是用Vuetify做的，架構參考其他pocaster的網頁，有主頁/home，還有關於/about、所有單集/episodes、文章/articles，以及文章中各篇的分頁，共五個分頁。</p>
          <p>6個單集中，只有第一集是實際的內容，其他是為了練習寫網頁加入的假集數。假集數的文字介紹來自維基百科。</p>
          <p>所有單集的頁面是最難做的。</p>
          <p>播出音訊的部分我試了很久，參考Youtuber Bibek的教學影片，再自己邊試邊改了很多次才成功運作，又加上單集簡介的overlay跟bottom sheets做的播放器。</p>
          <p>播放器還有一些小問題沒解決，像是我原本想加播放進度條，並讓音訊暫停之後可以從暫停處繼續播，但時間關係目前只能做到這樣。</p>
          <p>也想加背景的圖或引入animation.css做動畫，但一直失敗，也因為時間關係先停在這裡，因為前面的東西有點寫太久。</p>
          <p>響應式的部分，是參考幾個教學影片的結果，但我想應該有更好的寫法。</p>
          <p>以上。</p>
        </body-1>
      </v-flex>
    </v-layout>


  </v-content>
</template>

<script>
export default {
  name: 'About',

  components: {

  },

  data: () => ({
  
  }),
};
</script>
<style>

.concept {
  padding-top: 15px;
  padding-bottom: 15px;
}


</style>


