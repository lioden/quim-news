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
          v-for="(item, i) in sidemenu"
          :key="i"
          router
          @click="sideHandler(item.to)"
        >
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title" />
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar
      style="background-color:white"
      :clipped-left="clipped"
      fixed
      app
      height="80"
      :extension-height="extensionheight"
    >
      <div class="burguer">
        <v-btn icon @click.stop="drawer = !drawer">
          <v-icon class="burguericon">view_headline</v-icon>
        </v-btn>
      </div>
      <nuxt-link to="/">
        <v-toolbar-title class="padtop padleft">
          <img src="https://www.loba.pt/images/loba.png" alt="LOBA" />
        </v-toolbar-title>
      </nuxt-link>
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
          @input="handler(lang)"
        ></v-select>
      </v-toolbar-items>
      <template v-slot:extension style="align-items: center">
        <v-layout row wrap>
          <v-flex v-for="(item, i) in items" :key="i">
            <div class="outerbutton">
              <div class="button">
                <nuxt-link :to="item.to">
                  <div class="buttontext">{{ item.title }}</div>
                </nuxt-link>
              </div>
            </div>
          </v-flex>
        </v-layout>
      </template>
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
      extensionheight: '50',
      languages: ['en', 'pt'],
      categoria: ['cultura', 'desporto'],
      lang: 'pt',
      dark: false,
      clipped: true,
      drawer: false,
      fixed: false,
      items: [],
      sidemenu: [],
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
    this.handler('pt')
  },
  methods: {
    getTopmenu: function(idioma) {
      const self = this
      self.items = []
      axios
        .get('http://gateway.loba.pt:3001/rest/menutree/pt/menu_principal')
        .then(function(response) {
          for (const i in response.data.menutree) {
            if (response.data.menutree[i].title_langs[idioma] != null) {
              self.items.push({
                title: response.data.menutree[i].title_langs[idioma],
                to: response.data.menutree[i].link_langs[idioma]
              })
            }
          }
        })
    },
    buildRoute: function(route) {
      return this.lang + '/' + route
    },
    getSideMenu: function(lang) {
      const self = this
      self.sidemenu = []
      axios
        .get('http://gateway.loba.pt:3001/rest/menutree/pt/lateral')
        .then(function(response) {
          for (const i in response.data.menutree) {
            if (response.data.menutree[i].title_langs[lang] != null) {
              self.sidemenu.push({
                title: response.data.menutree[0].title_langs[lang],
                to: response.data.menutree[0].slug_langs[lang]
              })
            }
          }
        })
    },
    handler: function(idioma) {
      this.getTopmenu(idioma)
      this.getSideMenu(idioma)
    },
    sideHandler: function(route) {
      console.log(this.lang + '/' + route)
      this.$router.replace('/')
      this.$router.replace('pt/categoria')
      console.log(this.$router.app._route)
      let drawer = this.drawer
      drawer = !drawer
      this.drawer = drawer
    }
  }
}
</script>

<style media="screen">
a {
  text-decoration: none;
}
.margens {
  padding-top: 150px;
  margin: 30px 30px;
}
.burguer {
  padding-top: 12px;
}
.burguericon {
  padding-left: 1px;
}
.padtop {
  padding-top: 20px;
}
.padleft {
  padding-left: 10px;
}
.button:hover {
  background-position: left bottom;
}

.buttontext {
  border-style: solid;
  border-width: 1px;
  border-color: #c0c0c0;
  font-weight: bold;
  text-transform: uppercase;
  text-align: center;
  font-size: 15px;
  line-height: 50px;
  color: black;
  transition: all 0.6s ease-out;
  display: block;
}

.buttontext:hover {
  color: white;
  text-shadow: 0px 1px 2px grey;
}
</style>
