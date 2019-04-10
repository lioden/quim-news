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
      <v-toolbar-title class="padtop">
        <img src="https://www.loba.pt/images/loba.png" alt="LOBA" />
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-items class="padtop">
        <v-select
          v-model="lang"
          style="width:80px"
          :items="languages"
          label="lang"
          single-line
          return-object
          solo
          @input="changeLang(lang)"
        ></v-select>
      </v-toolbar-items>
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
import axios from 'axios'
import customfooter from '~/components/customfooter'
export default {
  components: {
    customfooter
  },
  data() {
    return {
      languages: ['en', 'pt'],
      categoria: ['cultura', 'desporto'],
      lang: 'pt',
      dark: false,
      clipped: true,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'nature_people',
          title: 'Cultura',
          to: '/pt/categorias/cultura'
        },
        {
          icon: 'directions_run',
          title: 'Desporto',
          to: '/pt/categorias/desporto'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      logo: 'https://i.ibb.co/gj4bRKq/quimlogo.png'
    }
  },
  mounted: function() {
    const self = this
    self.languages = []
    axios
      .get('http://gateway.loba.pt:3001/rest/languages')
      .then(function(response) {
        for (const index in response.data.languages)
          self.languages.push(response.data.languages[index].shortname)
      })
  },
  methods: {
    changeLang: function(potato) {
      console.log('log before potato')
      console.log(potato)
      console.log('log after potato')
      console.log(this.items[0].to)
      this.items[0].to = '/' + potato + '/categorias/' + this.categoria[0]
      console.log(this.items[0].to)
    }
  }
}
</script>

<style media="screen">
.margens {
  padding-top: 80px;
  margin: 30px 30px;
}
.padtop {
  padding-top: 8px;
}
</style>
