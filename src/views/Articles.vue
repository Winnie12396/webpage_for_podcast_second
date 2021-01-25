<template>
  <v-content class="articles">
    <v-layout row wrap justify-center pt-10>
      <v-flex xs10 sm8 md6>
        <v-card
          color="#CAF0FF"
        >
          <v-card-title class="headline">
            第一集後記
          </v-card-title>

          <v-card-subtitle>2021/1/24</v-card-subtitle>
          <v-card-text>哈囉大家好！這裡是天空裡的魚，我是Kite~ 在網站的關於頁面裡有提到，第一集「今天是生物藝術！」是我的一個期末作業，由於做了滿長一段時間，所以終於上架的時候覺得有點感動。也決定有空要寫個後記做記錄...</v-card-text>

          <v-card-actions>
            <v-btn text href="/article-afterword">
              繼續閱讀
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center pt-15>
      <v-flex xs10 sm8 md6>
        <v-card
          color="#CAF0FF"
        >
          <v-card-title class="headline">
            食譜分享：虱目魚皮湯
          </v-card-title>

          <v-card-subtitle>2021/1/24</v-card-subtitle>
          <v-card-text>這是我寒假跟我媽學的第一道菜！簡單又好喝~ 材料： 家樂福的冷凍虱目魚皮1包 芹菜一小把，切碎備用 薑絲...</v-card-text>

          <v-card-actions>
            <v-btn text href="/article-recipe-soup">
              繼續閱讀
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>

  </v-content>
</template>

<script>
export default {
  name: 'Articles',

  components: {

  },

  data: () => ({
  
  }),
};
</script>

