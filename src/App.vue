<template>
  <v-app>
    <AppTopBar/>
    <v-main>
      <router-view/>
    </v-main>
    <AppBottomBar/>
  </v-app>
</template>

<script>
import AppTopBar from "./components/shared/AppTopBar.vue"
import AppBottomBar from "./components/shared/AppBottomBar.vue"

export default {
  name: 'App',

  components : {
    AppTopBar,
    AppBottomBar
  }

};
</script>
