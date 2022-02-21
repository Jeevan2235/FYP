<template>
  <v-container>
    <v-row>
      <v-col v-for="link in links" :key="link" cols="12" md="4">
        <v-card
          class="d-flex flex-column justify-end"
          min-height="400"
          elevation="0"
          width="100%"
          :img="link.img"
          to="/blogsingle"
        >
          <v-card color="transparent" width="90%" tile elevation="0">
            <v-container class="ma-3">
              <p class="font-weight-black" style="color: #24cb83">
                {{ link.txt }}
              </p>
              <p class="white--text" style="font-size: 18px">
                {{ link.text }}
              </p>
              <p class="white--text">{{ link.date }}</p>
            </v-container>
          </v-card>
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
        img: "3.jpg",
        txt: "PHOTOGRAPHY",
        text: "The Social Art of Zaha Hadid, Architecture’s Most Engaging Presence",
        date: "2021, January 1",
      },
      {
        img: "3.jpg",
        txt: "PHOTOGRAPHY",
        text: "The Social Art of Zaha Hadid, Architecture’s Most Engaging Presence",
        date: "2021, January 1",
      },
      {
        img: "3.jpg",
        txt: "PHOTOGRAPHY",
        text: "The Social Art of Zaha Hadid, Architecture’s Most Engaging Presence",
        date: "2021, January 1",
      },
    ],
  }),
};
</script>

<style></style>
