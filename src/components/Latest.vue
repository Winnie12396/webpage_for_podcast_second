<template>
  <v-container>
    <div class="titleofthispart">
      <h2>最新單集</h2>
    </div>
    
    <div class="latest flex-no-wrap justify-space-between">

      
      <v-card
        class="mx-auto"
        max-width="336"
      >
        <v-img
          class="align-end"
          :aspect-ratio="1/1"
          src="@/assets/logo.png"
        >
        </v-img>
        <v-card-title>Ep.6 今天是古典樂！</v-card-title>
        <v-card-subtitle>來聽巴哈的郭德堡變奏曲</v-card-subtitle>

        <v-card-text>
          《郭德堡變奏曲》（德語：Goldberg-Variationen，BWV 988），是巴哈晚期的一部鍵盤作品，1741年出版。全曲32段，全部演出40-80分鐘。

          這部作品長期不受人們重視，直到20世紀前半葉女大鍵琴家蘭多夫斯卡的公開演奏及錄音。之後，1955年加拿大鋼琴家格倫·古爾德將其選作自己的第一張錄音作品。而現在，哥德堡變奏被視為巴赫作品中最重要的變奏曲之一。全作品包括主題，30個變奏，主題反覆。
        </v-card-text>
      </v-card>
      
    </div>
  </v-container>
</template>

<script>
  export default {
    name: 'Latest',

    data: () => ({
    }),
  }
</script>

<style>

.titleofthispart {

  padding-top: 12%;
  padding-bottom: 2%;
  text-align: center;
}


</style>

