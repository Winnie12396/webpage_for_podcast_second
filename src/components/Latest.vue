<template>
  <v-container>
    <div class="flex-no-wrap justify-space-between">

      
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
        <v-card-title>天空裡的魚</v-card-title>
        <v-card-subtitle>播客</v-card-subtitle>

        <v-card-text>
          Phasellus magna. Quisque rutrum. Nunc egestas, augue at pellentesque laoreet, felis eros vehicula leo, at malesuada velit leo quis pede. Aliquam lobortis. Quisque libero metus, condimentum nec, tempor a, commodo mollis, magna.

          In turpis. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. In turpis. Pellentesque dapibus hendrerit tortor. Ut varius tincidunt libero.
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
