<template>
  <div>
    <v-card tile elevation="0">
      <v-container>
        <v-row justify="center" class="mt-16">
          <v-col  md="6">
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
          </v-col>
          <v-col md="5">
            <h1>Airlines</h1>
          </v-col>
          <v-col md="1">
            <v-btn class="mx-2" fab dark small color="pink">
              <v-icon dark> mdi-magnify </v-icon>
            </v-btn>
          </v-col>
        </v-row>
        <v-row>
          <v-col v-for="link in links" :key="link" cols="12" md="4">
            <v-card
            to="/blogsingle"
              class="d-flex flex-column justify-end"
              min-height="400"
              elevation="0"
              width="100%"
              :img="link.img"
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
    </v-card>
  </div>
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

<style>
</style>