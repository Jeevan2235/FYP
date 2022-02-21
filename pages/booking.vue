<template>
  <div>
    <div class="flight">
      <v-container>
        <v-row>
          <v-col cols="12" md="2">
            <v-card-text class="text-subtitle-1">From</v-card-text>
            <v-select :items="items" outlined label="Houston Texas"></v-select>
          </v-col>
          <v-col cols="12" md="2">
            <v-card-text class="text-subtitle-1">To</v-card-text>
            <v-select :items="items" outlined label="Colorado"></v-select>
          </v-col>
          <v-col cols="12" md="2">
            <v-card-text class="text-subtitle-1">Departure Date</v-card-text>
            <v-select :items="items" outlined label="22nd February"></v-select>
          </v-col>
          <v-col cols="12" md="2">
            <v-card-text class="text-subtitle-1">Adult</v-card-text>
            <v-select :items="items" outlined label="2"></v-select>
          </v-col>
          <v-col cols="12" md="2">
            <v-card-text class="text-subtitle-1">Child</v-card-text>
            <v-select :items="items" outlined label="1"></v-select>
          </v-col>
          <v-col cols="12" md="2">
            <v-btn
              height="4em"
              color="#15aabe"
              class="mt-14 white--text mb-5"
              to="/booking"
              >Search Flights</v-btn
            >
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="ticket">
      <v-container>
        <v-row>
          <v-col md="3">
            <v-card class="mt-16" elevation="0">
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header>
                    <h3>Departure</h3>
                  </v-expansion-panel-header>
                  <v-expansion-panel-content>
                    <v-row >
                      <v-btn
                        v-for="link in links"
                        :key="link"
                        class="ma-2"
                        tile
                        elevation="0"
                        >{{ link }}</v-btn
                      >
                    </v-row>
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
              <v-divider ></v-divider>
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header>
                    <h3>Arrival</h3>
                  </v-expansion-panel-header>
                  <v-expansion-panel-content>
                    <v-row >
                      <v-btn
                        v-for="thing in things"
                        :key="thing"
                        class="ma-2"
                        tile
                        elevation="0"
                        >{{ thing }}</v-btn
                      >
                    </v-row>
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
              <v-divider ></v-divider>
              <v-expansion-panels>
  
              <v-expansion-panel>
                <v-expansion-panel-header>
                  <h3 >Airlines</h3>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  <v-row>
                <v-checkbox></v-checkbox>
                <p class="mt-5">American Airlines</p>
              </v-row>
              <v-row>
                <v-checkbox></v-checkbox>
                <p class="mt-5">American Airlines</p>
              </v-row>
              <v-row>
                <v-checkbox></v-checkbox>
                <p class="mt-5">American Airlines</p>
              </v-row>
                </v-expansion-panel-content>
              </v-expansion-panel>
                </v-expansion-panels>
            </v-card>
          </v-col>
          <v-col md="9">
            <h2 class="text-center">Houston Texas To Seattle</h2>

            <v-card
              class="mt-10"
              v-for="flight in flights"
              :key="flight"
              elevation="0"
            >
              <div class="ma-8">
                <v-row>
                  <v-col class="mt-8" md="2">
                    <v-img :src="flight.img" height="70%" width="60%"></v-img>
                  </v-col>
                  <v-col class="mt-8">
                    <p style="font-size: 1.3125rem; font-weight: 500">
                      {{ flight.time }}
                    </p>
                    <p>{{ flight.place }}</p>
                  </v-col>
                  <v-col class="mt-8">
                    <p>{{ flight.duration }}</p>
                  </v-col>
                  <v-col class="mt-8">
                    <p style="font-size: 1.3125rem; font-weight: 500">
                      {{ flight.time2 }}
                    </p>
                    <p>{{ flight.place2 }}</p>
                  </v-col>
                  <v-col class="mt-8">
                    <div class="text-center">
                      <p>{{ flight.price }}</p>
                      <v-btn outlined color="#00c9a7" to="/seat">{{ flight.btn }}</v-btn>
                    </div>
                  </v-col>
                </v-row>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    links: ["4AM-9AM", "6AM-9AM", "3AM-9AM", "4AM-9AM"],
    things: ["4AM-9AM", "6AM-9AM", "3AM-9AM", "4AM-9AM"],

    flights: [
      {
        img: "buddha.png",
        time: "08:30 AM",
        place: "Houston Texas",
        duration: "45 mins",
        time2: "09:15 AM",
        place2: "Seattle",
        price: "$200",
        btn: "Book Now",
      },
      {
        img: "buddha.png",
        icon: "mdi-facebook",
        time: "08:30 AM",
        place: "Houston Texas",
        duration: "45 mins",
        time2: "09:15 AM",
        place2: "Seattle",
        price: "$200",
        btn: "Book Now",
      },
      {
        img: "buddha.png",
        icon: "mdi-facebook",
        time: "08:30 AM",
        place: "Houston Texas",
        duration: "45 mins",
        time2: "09:15 AM",
        place2: "Seattle",
        price: "$200",
        btn: "Book Now",
      },
      {
        img: "buddha.png",
        icon: "mdi-facebook",
        time: "08:30 AM",
        place: "Houston Texas",
        duration: "45 mins",
        time2: "09:15 AM",
        place2: "Seattle",
        price: "$200",
        btn: "Book Now",
      },
      {
        img: "buddha.png",
        icon: "mdi-facebook",
        time: "08:30 AM",
        place: "Houston Texas",
        duration: "45 mins",
        time2: "09:15 AM",
        place2: "Seattle",
        price: "$200",
        btn: "Book Now",
      },
      {
        img: "buddha.png",
        icon: "mdi-facebook",
        time: "08:30 AM",
        place: "Houston Texas",
        duration: "45 mins",
        time2: "09:15 AM",
        place2: "Seattle",
        price: "$200",
        btn: "Book Now",
      },
    ],
  }),
};
</script>

<style>
.flight {
  background-color: #69f5ff;
}

.ticket {
  background-color: #e1e7ee;
}
</style>
