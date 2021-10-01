<template>
  <v-app>
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
       Doe um livro</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
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
  </v-app>
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
