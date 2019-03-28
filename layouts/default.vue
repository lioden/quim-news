<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-tile
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title" />
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar :clipped-left="clipped" fixed app>
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>web</v-icon>
      </v-btn>
      <v-toolbar-title>
        <img :src="logo" style="padding-top:8%" />
      </v-toolbar-title>
      <v-spacer />
    </v-toolbar>
    <v-content
      style="background-image: linear-gradient(to bottom, #5a5a5a, white, white, #616161);"
    >
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-tile @click.native="right = !right">
          <v-list-tile-action>
            <v-icon light>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <customfooter></customfooter>
  </v-app>
</template>

<script>
import customfooter from '~/components/customfooter'
export default {
  components: {
    customfooter
  },
  data() {
    return {
      dark: false,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'business',
          title: 'Página Principal',
          to: '/'
        },
        {
          icon: 'directions_run',
          title: 'Desporto',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      logo: 'https://www.loba.pt/images/loba.png'
    }
  }
}
</script>
