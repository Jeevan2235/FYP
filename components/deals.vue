<template>
  <v-container>
    <v-row  justify="center">
      <v-col cols="12" md="3" v-for="link in links" :key="link">
        <v-card class="mb-16" elevation="1" to="/flights">
          <v-img :src="link.img" height="250"> </v-img>
          <v-card-title>{{ link.title }}</v-card-title>
          <v-card-text>{{ link.text }}</v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    links: [
      {
        img: "pokhara.jpg",
        title: " Texas To Colorado",
        text: "Round Trip",
      },
      {
        img: "bhojpur.jpg",
        title: "Miami To Florida",
        text: "Round Trip",
      },
      {
        img: "muktinath.jpg",
        title: "New York To Chicago",
        text: "Round Trip",
      },
      {
        img: "lukla.jfif",
        title: "California To Alaska",
        text: "Round Trip",
      },
    ],
  }),
};
</script>

<style></style>
