<template>
  <div>
    <!-- Primeira Grid -->
    <v-container fluid grid-list-sm>
      <v-layout row wrap>
        <v-flex d-flex xs12 md9>
          <v-layout row wrap>
            <v-flex d-flex xs12 md12>
              <v-flex d-flex xs12 md12>
                <v-layout row wrap>
                  <v-flex d-flex xs12 md12>
                    <v-card color="grey lighten-3" dark>
                      <v-card-text class="black--text display-2 text-xs-center">
                        {{ location }}
                      </v-card-text>
                      <v-card-text class="black--text headline text-xs-center">
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
            <v-flex d-flex xs12 md12>
              <v-layout row wrap>
                <v-flex d-flex xs12 md12>
                  <v-card color="grey lighten-3" dark>
                    <v-img height="500px" :src="image"></v-img>
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
          <related
            :relatedtitles="relatedTitles"
            :relatedimages="relatedImages"
            sectiontitle="Notícias Relacionadas"
          ></related>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Fim da primeira grid -->
  </div>
</template>

<script>
import related from '~/components/related'
import axios from 'axios'
export default {
  components: {
    related
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    identificador: '',
    relatedImages: [],
    relatedTitles: [],
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
        for (const i in self.array[0].data.related_collections.results) {
          self.relatedTitles.push(
            self.array[0].data.related_collections.results[i].cover_photo
              .alt_description
          )
          self.relatedImages.push(
            self.array[0].data.related_collections.results[i].cover_photo.urls
              .regular
          )
        }
        console.log(self.relatedTitles)
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
