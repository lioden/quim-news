<template>
  <div>
    <v-layout align-center>
      <v-flex xs12 sm4 text-xs-center>
        <v-layout row wrap>
          <v-flex v-forxs12 sm12 text-xs-center>
            <nuxt-link :to="`/articles/${blocoids[0]}`">
              <v-hover>
                <v-card
                  slot-scope="{ hover }"
                  class="mx-auto"
                  color="grey lighten-4"
                >
                  <v-img height="500px" :src="blocourls[0]">
                    <v-expand-transition>
                      <div
                        v-if="hover"
                        class="d-flex red darken-2 v-card--reveal display-1 white--text"
                        style="height: 50%;"
                      >
                        {{ blocoids[0] }}
                      </div>
                    </v-expand-transition>
                  </v-img>
                </v-card>
              </v-hover>
            </nuxt-link>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <v-layout row wrap>
          <v-flex xs12 sm12 text-xs-center>
            <v-hover>
              <v-card
                slot-scope="{ hover }"
                class="mx-auto"
                color="grey lighten-4"
              >
                <v-img height="500px" :src="blocourls[0]">
                  <v-expand-transition>
                    <div
                      v-if="hover"
                      class="d-flex red darken-2 v-card--reveal display-1 white--text"
                      style="height: 50%;"
                    >
                      {{ blocoids[0] }}
                    </div>
                  </v-expand-transition>
                </v-img>
              </v-card>
            </v-hover>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <v-layout row wrap>
          <v-flex xs12 sm12 text-xs-center>
            <v-hover>
              <v-card
                slot-scope="{ hover }"
                class="mx-auto"
                color="grey lighten-4"
              >
                <v-img height="500px" :src="blocourls[0]">
                  <v-expand-transition>
                    <div
                      v-if="hover"
                      class="d-flex red darken-2 v-card--reveal display-1 white--text"
                      style="height: 50%;"
                    >
                      {{ blocoids[0] }}
                    </div>
                  </v-expand-transition>
                </v-img>
              </v-card>
            </v-hover>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
    <v-layout align-center>
      <v-flex xs12 sm4 text-xs-center>
        <div>
          <v-btn flat color="white" @click="pedido('sports')">sports</v-btn>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div>
          <v-btn flat color="white" @click="pedido('culture')">culture</v-btn>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div>
          <v-btn flat color="white" @click="pedido('business')">business</v-btn>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div>
          <v-btn flat color="white" @click="pedido('entertainment')"
            >entertainment</v-btn
          >
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div>
          <v-btn flat color="white" @click="pedido('technology')"
            >technology</v-btn
          >
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div>
          <v-btn flat color="white" @click="pedido('education')"
            >education</v-btn
          >
        </div>
      </v-flex>
    </v-layout>
    <hr class="grey--text" />
    <v-container fluid grid-list>
      <v-layout row wrap>
        <v-flex d-flex xs12 sm6 md4 style="height:1200px">
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link :to="`/articles/${blocoids[0]}`"
                    ><v-img style="height:400px" :src="blocourls[0]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link :to="`/articles/${blocoids[1]}`"
                    ><v-img style="height:400px" :src="blocourls[1]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link :to="`/articles/${blocoids[2]}`"
                    ><v-img style="height:400px" :src="blocourls[2]"></v-img
                  ></nuxt-link>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 sm6 md3 style="height:1200px">
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12 style="height:600px">
                  <nuxt-link :to="`/articles/${blocoids[3]}`"
                    ><v-img style="height:600px" :src="blocourls[3]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:600px">
                  <nuxt-link :to="`/articles/${blocoids[4]}`"
                    ><v-img style="height:600px" :src="blocourls[4]"></v-img
                  ></nuxt-link>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs6 sm6 md3 style="height:1200px">
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link :to="`/articles/${blocoids[5]}`"
                    ><v-img style="height:400px" :src="blocourls[5]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link :to="`/articles/${blocoids[6]}`"
                    ><v-img style="height:400px" :src="blocourls[6]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link :to="`/articles/${blocoids[7]}`"
                    ><v-img style="height:400px" :src="blocourls[7]"></v-img
                  ></nuxt-link>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs6 sm6 md2 style="height:1200px">
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link :to="`/articles/${blocoids[8]}`"
                    ><v-img style="height:300px" :src="blocourls[8]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link :to="`/articles/${blocoids[9]}`"
                    ><v-img style="height:300px" :src="blocourls[9]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link :to="`/articles/${blocoids[0]}`"
                    ><v-img style="height:300px" :src="blocourls[0]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link :to="`/articles/${blocoids[1]}`"
                    ><v-img style="height:300px" :src="blocourls[1]"></v-img
                  ></nuxt-link>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data: () => ({
    dialog: false,
    blocourls: [],
    blocoids: [],
    array: []
    // categoria: 'football'
  }),
  created: function() {
    this.pedido('pugs')
  },
  methods: {
    pedido: function(categoria) {
      const self = this
      self.blocourls = []
      self.blocoids = []
      console.log(
        'https://api.unsplash.com/search/photos/?page=1;query=' +
          categoria +
          ';orientation=landscape;client_id=2ebf903d65d58846dba610108cbf428043756525989c37bfd1121174ff28a339'
      )
      axios
        .get(
          'https://api.unsplash.com/search/photos/?page=1;query=' +
            categoria +
            ';orientation=landscape;client_id=2ebf903d65d58846dba610108cbf428043756525989c37bfd1121174ff28a339'
        )
        .then(function(response) {
          console.log(response)
          self.array = []
          self.array.push(response)
          console.log('-------------------blocourls antes-------------------')
          console.log(self.blocourls)
          for (const index in self.array[0].data.results) {
            self.blocourls.push(self.array[0].data.results[index].urls.regular)
            self.blocoids.push(self.array[0].data.results[index].id)
          }
          console.log('-------------------blocourls depois-------------------')
          console.log(self.blocourls)
        })
        .catch(function(error) {
          console.log(error)
        })
    }
  }
}
</script>
<style media="screen">
a {
  padding: 0;
  margin: 0;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.8;
  position: absolute;
  width: 100%;
}

.custom {
  padding-top: 100px;
}
</style>
