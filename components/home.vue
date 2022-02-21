<template>
  <div>
    <div v-for="link in links" :key="link">
      <v-img :src="link.img">
        <h1
          class="text-center"
          style="
            font-size: 60px;
            font-family: Playfair Display, serif;
            color: #0e385d;
          "
        >
          {{ link.text }}
        </h1>
        <p
          class="text-center"
          style="
            font-size: 30px;
            font-family: Playfair Display, serif;
            color: #0e385d;
          "
        >
          {{ link.desc }}
        </p>

        <v-row justify="center">
          <v-card width="35em" class="mb-10 mt-5">
            <p
              class="text-center"
              style="
                font-size: 30px;
                font-family: Playfair Display, serif;
                color: #0e385d;
              "
            >
              Search for flights
            </p>
            <v-row class="ml-5 mt-5"> </v-row>
            <v-row>
              <v-col md="12" cols="12">
                <v-tabs background-color="transparent" dark color="white">
                  <v-tab>
                    <v-btn color="#15aabe" class="white--text">One Way</v-btn>
                  </v-tab>
                  <v-tab-item>
                    <v-card>
                      <oneway />
                    </v-card>
                  </v-tab-item>
                  <v-tab>
                    <v-btn color="#15aabe" class="ml-5 white--text"
                      >Two Way</v-btn
                    >
                  </v-tab>
                  <v-tab-item>
                    <v-card>
                      <twoway />
                    </v-card>
                  </v-tab-item>
                </v-tabs>
              </v-col>
            </v-row>
            
          </v-card>
        </v-row>
      </v-img>
    </div>
  </div>
</template>

<script>
import oneway from "./oneway.vue";
import Twoway from "./twoway.vue";
export default {
  components: { oneway, Twoway },

  data: () => ({
    links: [
      {
        text: "Book your next flight with us",
        img: "airport.png",
        desc: "Search from 100s of different flights that suites the best for your next trip",
      },
    ],

    methods: {
      switchAccountVue(value) {
        value == "login" ? (this.oneway = true) : (this.oneway = false);
      },
    },
  }),
};
</script>

<style></style>
