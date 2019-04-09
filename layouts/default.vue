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
          @click="drawer = !drawer"
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
    <v-toolbar :clipped-left="clipped" fixed app color="white">
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <!-- <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>web</v-icon>
      </v-btn> -->
      <nuxt-link to="/"
        ><v-btn icon>
          <v-icon>home</v-icon>
        </v-btn></nuxt-link
      >
      <v-toolbar-title>
        <img src="https://www.loba.pt/images/loba.png" alt="LOBA" />
      </v-toolbar-title>
      <v-spacer />
    </v-toolbar>
    <div>
      <div class="margens">
        <nuxt />
      </div>
    </div>
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
      clipped: true,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'whatshot',
          title: 'Recentes',
          to: '/'
        },
        {
          icon: 'nature_people',
          title: 'Cultura',
          to: '/categorias/cultura'
        },
        {
          icon: 'directions_run',
          title: 'Desporto',
          to: '/categorias/desporto'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      logo: 'https://i.ibb.co/gj4bRKq/quimlogo.png'
    }
  }
}
</script>

<style media="screen">
.margens {
  padding-top: 80px;
  margin: 30px 30px;
}
</style>
