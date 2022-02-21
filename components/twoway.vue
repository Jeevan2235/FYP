<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="4">
        <v-card-text>From</v-card-text>
        <v-select outlined></v-select>
      </v-col>
      <v-col cols="12" md="4">
        <v-card-text>To</v-card-text>
        <v-select outlined></v-select>
      </v-col>
      <v-col cols="12" md="4">
        <v-card-text>Departure Date</v-card-text>
        <v-select outlined>
          <!-- <v-row justify="center">
                      <v-date-picker v-model="picker"></v-date-picker>
                    </v-row> -->
        </v-select>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="4">
        <v-card-text>Return Date</v-card-text>
        <v-select outlined>
          <!-- <v-row justify="center">
                      <v-date-picker v-model="picker"></v-date-picker>
                    </v-row> -->
        </v-select>
      </v-col>
      <v-col cols="12" md="4">
        <v-card-text>Adult</v-card-text>
        <v-select outlined></v-select>
      </v-col>
      <v-col cols="12" md="4">
        <v-card-text>Child</v-card-text>
        <v-select outlined></v-select>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-btn height="4em" color="#15aabe" class="white--text mb-5" to="/booking"
        >Search Flights</v-btn
      >
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
</style>