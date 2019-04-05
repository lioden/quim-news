<template>
  <div>
    <v-layout align-center>
      <v-flex xs12 sm4>
        <div class="outerbutton">
          <div class="button" @click="pedido('culture')">
            <div class="buttontext">Cultura</div>
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div class="outerbutton">
          <div class="button" @click="pedido('sports')">
            <div class="buttontext">Desporto</div>
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div class="outerbutton">
          <div class="button" @click="pedido('education')">
            <div class="buttontext">Educação</div>
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div class="outerbutton">
          <div class="button" @click="pedido('science')">
            <div class="buttontext">Ciência</div>
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div class="outerbutton">
          <div class="button" @click="pedido('business')">
            <div class="buttontext">Negócios</div>
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm4 text-xs-center>
        <div class="outerbutton">
          <div class="button" @click="pedido('entertainment')">
            <div class="buttontext">Entretenimento</div>
          </div>
        </div>
      </v-flex>
    </v-layout>
    <hr color="grey" />
    <br />
    <v-layout>
      <v-flex xs12 sm4 text-xs-center>
        <v-layout row wrap>
          <v-flex
            v-for="(value, i) in blocourls.slice(0, 3)"
            :key="i"
            xs12
            sm12
            text-xs-center
            class="zoom"
          >
            <nuxt-link :to="`/articles/${blocoids[i]}`">
              <v-hover>
                <v-card
                  slot-scope="{ hover }"
                  class="mx-auto"
                  color="grey lighten-4"
                  style="height:400px"
                >
                  <v-img style="height:400px" :src="blocourls[i]">
                    <v-expand-transition>
                      <div
                        v-if="hover"
                        class="d-flex red darken-2 v-card--reveal display-1 white--text"
                        style="height: 50%;"
                      >
                        {{ blocoids[i] }}
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
          <v-flex
            v-for="(potato, b) in blocourls.slice(3, 7)"
            :key="(b = b + 3)"
            xs12
            sm12
            text-xs-center
            class="zoom"
          >
            <nuxt-link :to="`/articles/${blocoids[b]}`">
              <v-hover>
                <v-card
                  slot-scope="{ hover }"
                  class="mx-auto"
                  color="grey lighten-4"
                  style="height:300px"
                >
                  <v-img style="height:300px" :src="blocourls[b]">
                    <v-expand-transition>
                      <div
                        v-if="hover"
                        class="d-flex red darken-2 v-card--reveal display-1 white--text"
                        style="height: 50%;"
                      >
                        {{ blocoids[b] }}
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
          <v-flex
            v-for="(potato, b) in blocourls.slice(6, 9)"
            :key="(b = b + 7)"
            xs12
            sm12
            text-xs-center
            class="zoom"
          >
            <nuxt-link :to="`/articles/${blocoids[b]}`">
              <v-hover>
                <v-card
                  slot-scope="{ hover }"
                  class="mx-auto"
                  color="grey lighten-4"
                  style="height:400px"
                >
                  <v-img style="height:400px" :src="blocourls[b]">
                    <v-expand-transition>
                      <div
                        v-if="hover"
                        class="d-flex red darken-2 v-card--reveal display-1 white--text"
                        style="height: 50%;"
                      >
                        {{ blocoids[b] }}
                      </div>
                    </v-expand-transition>
                  </v-img>
                </v-card>
              </v-hover>
            </nuxt-link>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
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
    this.pedido('aveiro')
  },
  methods: {
    pedido: function(categoria) {
      const self = this
      self.blocourls = []
      self.blocoids = []
      axios
        .get(
          'https://api.unsplash.com/search/photos/?page=1;query=' +
            categoria +
            ';client_id=2ebf903d65d58846dba610108cbf428043756525989c37bfd1121174ff28a339'
        )
        .then(function(response) {
          self.array = []
          self.array.push(response)
          for (const index in self.array[0].data.results) {
            self.blocourls.push(self.array[0].data.results[index].urls.regular)
            self.blocoids.push(self.array[0].data.results[index].id)
            console.log('--------------blocorurls------------------')
            console.log(self.blocourls)
          }
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
.zoom {
  transition: transform 0.5s; /* Animation */
  margin: 0 auto;
}

.zoom:hover {
  z-index: 1;
  transform: scale(
    1.1
  ); /* Note: if the zoom is too large, it will go outside of the viewport) */
}

.outerbutton {
  margin: 0px 0px;
}
.button {
  cursor: pointer;
  border-radius: 0px;
  width: 100%;
  height: 100%;
  display: block;

  background: linear-gradient(to right, black 50%, transparent 50%);
  background-size: 200% 100%;
  background-position: right bottom;
  transition: all 0.3s ease-out;
}

.button:hover {
  background-position: left bottom;
}

.buttontext {
  font-weight: bold;
  text-shadow: 0px 1px 2px black;
  text-transform: uppercase;
  text-align: center;
  font-size: 15px;
  line-height: 50px;
  color: white;
  transition: all 0.6s ease-out;
  display: block;
}

.buttontext:hover {
  color: white;
  text-shadow: 0px 1px 2px grey;
}
</style>
