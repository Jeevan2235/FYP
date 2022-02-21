<template>
  <div>
    <v-img src="wing.jpg"> </v-img>
    <h1 class="text-center mt-16" style="font-family: Playfair Display, serif; color: #0e385d">Overview of Texas To Colorado</h1>
    <v-container>
      <p class="mt-10" style="text-align: justify">
        Colorado is the ideal winter destination with unparalleled skiing and
        snowboarding, snowshoeing, snowmobiling, fat-biking, snowtubing,
        seasonal festivals, a rich cultural heritage and so much more. Plan your
        Colorado vacation now and find out if you're Colo-Ready! The scenic
        byways of Colorado connect the dots between historic sites and acres of
        majestic scenery that span red-rock canyons, the peaks of the Rocky
        Mountains and sun-kissed prairies. Find videos, trip tips, itineraries
        and more.
      </p>
    </v-container>
    <flightdetails />
    <div>
      <template>

        
        
        
</template>
    </div>
  </div>
</template>

<script>
import flightdetails from "~/components/flightdetails.vue";
import Oneway from '../components/oneway.vue';
import Twoway from '../components/twoway.vue';
export default {
  components: { flightdetails, Oneway, Twoway },
  data () {
      return {
        tabs: null,
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
        text1: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequatjeevan.',
      }
    },
};
</script>

<style></style>
