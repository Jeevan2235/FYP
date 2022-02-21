<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" temporary app right color="#0c2059">
      <h2
        class="pa-2 white--text text-center"
        v-for="i in ['Home', 'About Us', 'Blog', 'Flights', 'Contact Us']"
        :key="i"
      >
        {{ i }}
      </h2>
    </v-navigation-drawer>
    <div class="heading">
      <v-row no-gutters>
        <v-spacer></v-spacer>
        <div v-if="!isSmallEnough">
          <v-btn
            v-for="link in links"
            :key="link"
            text
            rounded
            class="mx-5 mt-3 white--text"
            link
            :to="i == 0 ? '/' : '/' + link.toLowerCase()"
          >
            {{ link }}
          </v-btn>
          <v-btn
            class="mx-16 my-2 white--text"
            outlined
            elevation="0"
            height="4em"
            to="/signup"
          >
            <v-icon>mdi-account</v-icon> Sign In / Register</v-btn
          >
        </div>
        <v-app-bar-nav-icon
          v-else
          class="mt-4"
          @click="drawer = !drawer"
        ></v-app-bar-nav-icon>
      </v-row>
    </div>

    <v-main>
      <Nuxt />
    </v-main>
    <v-footer>
      <v-container>
        <v-row class="mt-5">
          <v-col cols="12" md="4" sm="6">
            <h2 style="color: #0596c8">About</h2>
            <v-divider class="mt-3"></v-divider>
            <v-img src="footer-logo.png" height="50" width="245"> </v-img>
            <p class="">
              We Provide Premium Word Press, Ghost and HTML template. Our Perm
              tritium Templates is, develop gaped in a way so that the clients
              find Support. Themes are developed in a way so that the clients
              find.
            </p>
            <v-btn class="white--text" color="#0596c8" width="130" height="40"
              >More</v-btn
            >
          </v-col>

          <v-col cols="12" md="4" sm="6">
            <h2 style="color: #0596c8">Place Category</h2>
            <v-divider class="mb-12 mt-3"></v-divider>
            <p style="text-bold">
              Flat for Rent <span style="color: #0596c8">Francis</span>
            </p>
            <p>Flat for Rent <span style="color: #0596c8">Collins St</span></p>
            <p>Flat for Rent <span style="color: #0596c8">Rose Ln</span></p>
            <p>Flat for Rent <span style="color: #0596c8">Cosgrave Ln</span></p>
            <p>Flat for Rent <span style="color: #0596c8">Bourke St</span></p>
            <p>
              Flat for Rent <span style="color: #0596c8">Flienders Ln</span>
            </p>
          </v-col>
          <v-col cols="12" md="4" sm="6">
            <h2 style="color: #0596c8">Instagram Image</h2>
            <v-divider class="mb-12 mt-3"></v-divider>
            <v-row>
              <v-col v-for="n in 6" :key="n" class="d-flex child-flex" cols="4">
                <v-img
                  :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                  :lazy-src="`https://picsum.photos/10/6?image`"
                  aspect-ratio="1"
                  class="grey lighten-2"
                >
                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>
                </v-img>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  methods: {
    onResize() {
      this.windowSize = { x: window.innerWidth, y: window.innerHeight };
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", () => {
      this.onResize();
    });
  },
  computed: {
    isSmallEnough() {
      // return false
      return this.windowSize.x < 960 ? true : false;
    },
  },
  data: () => ({
    links: ["Home", "About Us", "Blog", "Flights", "Contact Us"],
    drawer: false,
    windowSize: {
      x: 0,
      y: 0,
    },
  }),
};
</script>

<style scoped>
.heading {
  background-color: #0596c8;
}
</style>
