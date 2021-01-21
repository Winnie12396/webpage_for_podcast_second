<template>
  <v-container>
    <v-row
      no-gutters
      align="center"
      align-content="center"
      justify="start"
    >
      <v-col
        v-for="item in items"
        :key="item.id"
        cols="4"
      >

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
          <v-card-title>{{ item.title }}</v-card-title>
          <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>

          <v-card-text>
            {{ item.text }}
          </v-card-text>
          <v-btn
            color="orange"
          >
            播放
          </v-btn>
        </v-card>
      </v-col>
    
    </v-row>

    
  </v-container>
</template>

<script>
  export default {
    name: 'Episodes',

    data: () => ({
      items: [
        {
          id: 1,
          title: "hey",
          subtitle: "",
          text: "",
          src: ""
        },
        {
          id: 2,
          title: "hi",
          subtitle: "",
          text: "",
          src: ""
        },
        {
          id: 3,
          title: "ho",
          subtitle: "",
          text: "",
          src: ""
        },
      ]
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