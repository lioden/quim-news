<template>
  <div>
    <div v-for="(value, i) in array" :key="i">
      <v-flex d-flex xs6 md6>
        <v-layout row wrap>
          <v-flex d-flex xs12 md12>
            <v-card color="grey lighten-3" dark>
              <v-img height="500px" :src="getImg(value.image_desktop)"></v-img>
              <br />
              <v-card-text class="black--text subheading">
                <p></p>
              </v-card-text>
              <v-card-text class="black--text headline text-xs-right">
                Autor: {{ value.subtitle_langs.pt }}
              </v-card-text>
              <v-card-text class="black--text caption text-xs-right">
                Tags: Placeholder
              </v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data: () => ({
    array: []
  }),
  mounted: function() {
    const self = this
    axios
      .get('http://gateway.loba.pt:3001/rest/banners/pt/Desporto')
      .then(function(response) {
        self.array = response.data.banners
        console.log(self.array)
      })
  },
  methods: {
    getImg: function(path) {
      console.log('http://cms.loba.pt' + path)
      return 'http://cms.loba.pt' + path
    }
  }
}
</script>
