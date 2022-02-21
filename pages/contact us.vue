<template>
  <div>
    <div v-for="link in links" :key="link">
      <v-img :src="link.img" height="30em"></v-img>

      <v-row>
       <v-container>
          <callus />
        <contact />
       </v-container>
      </v-row>
    </div>
  </div>
</template>

<script>
import Callus from "~/components/callus.vue";
import contact from "~/components/contact.vue";
export default {
  components: { contact, Callus },
  data: () => ({
    links: [
      {
        img: "contact.jpg",
      },
    ],
  }),
};
</script>

<style></style>
