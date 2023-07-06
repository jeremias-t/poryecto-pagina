<template>
  <v-app id="inspire">
    <v-app-bar
      app
      color="grey darken-4
"
      flat
    >
      <v-container class="py-0 fill-height">
        <v-btn v-for="link in links" :key="link" text class="white--text">
          {{ link }}
        </v-btn>

        <v-spacer></v-spacer>

        <v-responsive max-width="260">
          <v-text-field
            dense
            class="grey darken-1"
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive>
      </v-container>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app width="300" class="grey darken-3">
      <v-list-item>
        <v-list-item-title class="headline mt-16 white--text pl-8"
          >Lancer Work</v-list-item-title
        >
      </v-list-item>
      <v-list class="pt-16 pl-8" shaped>
        <v-list-item v-for="iten in itens" :key="iten" class="white--text" link>
          <v-list-item-content>
            <v-list-item-title> {{ iten }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main class="grey darken-4 main">
      <filtro-comp />
      <cartas-comp />
    </v-main>
  </v-app>
</template>

<style scoped>
li {
  text-decoration: none;
}

.main {
  padding: 0;
}
</style>

<script>
import CartasComp from "./cartas-comp.vue";
import filtroComp from "./filtro-comp.vue";
export default {
  components: { filtroComp, CartasComp },
  data: () => ({
    links: ["My Files", "Cloud", "Settings"],
    itens: ["Dashboard", "Conversation", "My store", "Candidates"],
  }),
  drawer: null,
};
</script>
