<template>
  <v-app>
    <v-main>
      <fondo-comp />
    </v-main>
  </v-app>
</template>

<script>
import FondoComp from "./components/fondo-comp.vue";

export default {
  name: "App",

  components: {
    FondoComp,
  },

  data: () => ({
    //
  }),
};
</script>
