<template>
<v-app>
 <v-bottom-navigation
    :value="value"
    color="primary"
  >
    <v-btn>
      <span>Recents</span>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>Favorites</span>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn>
      <span>Nearby</span>

      <v-icon>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>
  <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'AppBottomBar',

  data: () => ({
    value: 1
  }),
};
</script>
