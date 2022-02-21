<template>
  <div>
    <h2 class="text-center mt-10" style="font-size: 30px; font-family: Playfair Display, serif; color: #0e385d">Please Select Your Seat</h2>
    <v-container>
      <v-card class="mb-16">
        <v-row class="mt-16">
          <v-col v-for="link in links" :key="link" md="6">
            <v-select :items="items" label="Please Select Your Seat" outlined class="ma-8"></v-select>
            <p class="ma-4 text-center">{{ link.text }}</p>
            <div class="text-center mt-16">
              <v-btn elevation="1" color="#cbe8ff"> Continue To Payment </v-btn>
            </div>
          </v-col>
          <v-col md="6">
            <v-img src="seats.png"></v-img>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({

    items: ["1A", "1B", "1C", "1D", "1E", "1F"],

    links: [
      {
        text: "Selected Seats : 1D, 1F, 1A",
      },
    ],
  }),
};
</script>

<style>
</style>