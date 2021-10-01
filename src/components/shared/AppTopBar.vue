<template>
  <v-container>
      <v-app-bar
      color="deep-purple accent-4"
      app
      dark
      >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>
        <v-avatar size="24">
            <v-img src="http://www.educacao.al.gov.br/images/logo-01.png" size="25"/>
        </v-avatar>
       Doe um livro
      </v-toolbar-title>
      </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
        <v-list nav dense>
          <v-list-item-group v-model="group">
              
              <router-link to="/">
                  <v-list-item>
                      <v-list-item-icon>
                          <v-icon>mdi-home</v-icon>
                      </v-list-item-icon>
                      <v-list-item-title>
                          Início
                      </v-list-item-title>
                  </v-list-item>
              </router-link>

              <router-link to="/about">
                  <v-list-item>
                      <v-list-item-icon>
                          <v-icon>mdi-information</v-icon>
                      </v-list-item-icon>
                      <v-list-item-title>
                          Segunda aba
                      </v-list-item-title>
                  </v-list-item>
              </router-link>
          </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
  </v-container>
</template>

<script>
export default {
  name: 'AppTopBar',
  data() {
    return {
      drawer: false,
      group: null,
    }
  }
};
</script>
