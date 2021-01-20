<template>
  <v-container>
    <v-row
      v-for="n in 1"
      :key="n"
      no-gutters
      align="center"
      align-content="center"
      justify="start"
    >
      <v-col>

        <v-img
          class="align-end"
          max-width="350"
          :aspect-ratio="1"
          src="@/assets/logo-fish.jpg"
        >
        </v-img>
      </v-col>
    
    </v-row>

    
  </v-container>
</template>

<script>
  export default {
    name: 'Episodes',

    data: () => ({
    }),
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