<template>
  <v-container>

    <v-layout row wrap justify-center>
      <v-flex xs12 md4 xl3 py-10 my-8>
        <v-img
          max-width="350"
          :aspect-ratio="1"
          src="@/assets/logo-fish.jpg"
          transition="scroll-x-transition"
        >
        </v-img>
      </v-flex>   
      <v-flex xs12 md6 py-10 my-8>
        <v-card
          class="mx-auto"
          flat
        >
          <v-card-title><h4>天空裡的魚</h4></v-card-title>
          <v-card-subtitle>播客</v-card-subtitle>

          <v-card-text>
            <p>一個19歲大學女生，在一次期末作業之中突發奇想，也許可以來試試看做podcast這件事。</p>
            <p>主軸是跟吃有關的科學和其他事情，配上其他心血來潮的支線劇情~</p>

            <p>目前在Firstory、KKbox、Spotify、Apple Podcasts跟PocketCasts皆可收聽喔</p>
            <p>期待與你相見！</p>

            <p>有任何想聊的可以私訊 IG @fishinthesky1212 或寄信給我：fishinthesky1212@gmail.com</p>
          </v-card-text>
        </v-card>
      </v-flex> 
    </v-layout>    
  </v-container>
</template>

<script>
  export default {
    name: 'Intro',

    data: () => ({

    }),
  }
</script>

<style>

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
      <v-card
      class="mx-auto"
      color="primary"
      width="100vw"
    >
      <v-img
        class="align-center"
        max-width="350"
        :aspect-ratio="1"
        src="@/assets/logo-fish.jpg"
      >
      </v-img>
      <v-card

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
    </v-card>

-->

<!--
    <v-row
      v-for="n in 1"
      :key="n"
      no-gutters
      align="center"
      align-content="center"
      justify="start"
      flex
    >
      <v-col>

        <v-img
          class="align-end logo"
          max-width="350"
          :aspect-ratio="1"
          src="@/assets/logo-fish.jpg"
          transition="scroll-x-transition"
        >
        </v-img>

        
      </v-col>
      <v-col>
        <v-card
          class="mx-auto"
          max-width="350"
          flat
        >
          <v-card-title><h4>天空裡的魚</h4></v-card-title>
          <v-card-subtitle>播客</v-card-subtitle>

          <v-card-text>
            Phasellus magna. Quisque rutrum. Nunc egestas, augue at pellentesque laoreet, felis eros vehicula leo, at malesuada velit leo quis pede. Aliquam lobortis. Quisque libero metus, condimentum nec, tempor a, commodo mollis, magna.

            In turpis. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. In turpis. Pellentesque dapibus hendrerit tortor. Ut varius tincidunt libero.
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
-->