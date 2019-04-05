<template>
  <div>
    <!-- Primeira Grid -->
    <v-container fluid grid-list style="padding:2% 0px 2%">
      <v-layout row wrap>
        <v-flex d-flex xs12 md9>
          <v-layout row wrap>
            <v-flex d-flex xs12 md12>
              <v-flex d-flex xs12 md12>
                <v-layout row wrap>
                  <v-flex d-flex xs12 md12 style="padding-right:10px;">
                    <v-card color="grey lighten-3" dark>
                      <v-card-text
                        class="black--text display-2 text-xs-center"
                        style="padding-top:30px"
                      >
                        {{ location }}
                      </v-card-text>
                      <v-card-text
                        class="black--text headline text-xs-center"
                        style="padding-top:30px"
                      >
                        {{ subtitle }}
                      </v-card-text>
                      <v-card-text class="black--text caption text-xs-right">
                        {{ dia }}
                      </v-card-text>
                    </v-card>
                  </v-flex>
                </v-layout>
              </v-flex>
            </v-flex>
            <v-flex d-flex xs12 md4 style="padding-top:10px">
              <morevideos
                class="hidden-sm-and-down"
                title="Notícias Relacionadas"
              ></morevideos>
            </v-flex>
            <v-flex d-flex xs12 md8>
              <v-layout row wrap>
                <v-flex
                  d-flex
                  xs12
                  md12
                  style="padding-left:10px; padding-right:10px"
                >
                  <v-card color="grey lighten-3" dark>
                    <v-img :src="image"></v-img>
                    <br />
                    <hr />
                    <br />
                    <v-card-text class="black--text subheading">
                      <p>
                        {{ story }}
                      </p>
                    </v-card-text>
                    <v-card-text class="black--text caption text-xs-right">
                      Autor: {{ author }}
                    </v-card-text>
                    <v-card-text class="black--text caption text-xs-right">
                      Tags: Placeholder
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md3>
          <latestnews class="hidden-sm-and-down"></latestnews>
        </v-flex>
        <v-flex d-flex xs12 md4 style="padding-top:50px">
          <v-card color="grey darken-3" dark class="hidden-md-and-up">
            <morevideos title="Notícias relacionadas"></morevideos>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Fim da primeira grid -->
  </div>
</template>

<script>
import latestnews from '~/components/latestnews'
import morevideos from '~/components/morevideos'
import axios from 'axios'
export default {
  components: {
    latestnews,
    morevideos
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    identificador: '',
    array: [],
    id: 'placeholder',
    subtitle: '',
    author: '',
    location: 'No title given',
    story: '',
    dia: '',
    image: ''
  }),
  created: function() {
    this.identificador = this.$route.params.artigo
  },
  mounted: function() {
    const self = this
    axios
      .get(
        'https://api.unsplash.com/photos/' +
          self.identificador +
          '/?client_id=2ebf903d65d58846dba610108cbf428043756525989c37bfd1121174ff28a339'
      )
      .then(function(response) {
        self.array.push(response)
        self.id = self.array[0].data.id
        self.image = self.array[0].data.urls.regular
        self.location = self.array[0].data.location.title
        self.subtitle = self.array[0].data.alt_description
        self.dia = self.array[0].data.created_at
        self.story = self.array[0].data.story.title
        self.author = self.array[0].data.user.name
      })
  }
}
</script>
