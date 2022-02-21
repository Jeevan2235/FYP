<template>
  <div>
    <home />

    <h1
      class="mt-16 text-center"
      style="font-family: Playfair Display, serif; color: #0e385d"
    >
      Featured Flight Deals
    </h1>
    <div class="mt-10">
      <deals />
    </div>
    <maps />

    <h1
      class="mt-16 text-center"
      style="font-family: Playfair Display, serif; color: #0e385d"
    >
      Recent Blog Articles
    </h1>
    <div class="mt-10">
      <blog />

      <div class="text-center mt-12">
        <v-btn class="white--text mb-10" height="3.5em" color="blue" to="/blog">
          View All Blogs
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
import Deals from "~/components/deals.vue";
import home from "~/components/home.vue";
import Maps from "~/components/maps.vue";
export default {
  components: { home, Deals, Maps },
};
</script>

<style></style>
