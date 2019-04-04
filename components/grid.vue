<template>
  <div>
    <v-container fluid grid-list>
      <v-layout row wrap>
        <v-dialog v-model="dialog" width="600px">
          <template v-slot:activator="{ on }">
            <v-flex d-flex xs12 style="height:500px">
              <v-img
                style="object-fit: contain;"
                :src="blocourls[0]"
                v-on="on"
              ></v-img>
            </v-flex>
          </template>
          <v-card>
            <v-card-title>
              <span class="headline">Use Google's location service?</span>
            </v-card-title>
            <v-card-text
              >Lorem ipsum dolor sit amet, semper quis, sapien id natoque elit.
              Nostra urna at, magna at neque sed sed ante imperdiet, dolor
              mauris cursus velit, velit non, sem nec. Volutpat sem ridiculus
              placerat leo, augue in, duis erat proin condimentum in a eget, sed
              fermentum sed vestibulum varius ac, vestibulum volutpat orci ut
              elit eget tortor. Ultrices nascetur nulla gravida ante arcu.
              Pharetra rhoncus morbi ipsum, nunc tempor debitis, ipsum
              pellentesque, vitae id quam ut mauris dui tempor, aptent non.
              Quisque turpis. Phasellus quis lectus luctus orci eget rhoncus.
              Amet donec vestibulum mattis commodo, nulla aliquet, nibh
              praesent, elementum nulla. Sit lacus pharetra tempus magna neque
              pellentesque, nulla vel erat. Justo ex quisque nulla accusamus
              venenatis, sed quis. Nibh phasellus gravida metus in, fusce aenean
              ut erat commodo eros. Ut turpis, dui integer, nonummy pede placeat
              nec in sit leo. Faucibus porttitor illo taciti odio, amet viverra
              scelerisque quis quis et tortor, curabitur morbi a. Enim tempor
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn color="green darken-1" flat="flat" @click="dialog = false"
                >Disagree</v-btn
              >
              <v-btn color="green darken-1" flat="flat" @click="dialog = false"
                >Agree</v-btn
              >
            </v-card-actions>
          </v-card>
        </v-dialog>
        <v-flex d-flex xs12 sm6 md4 style="height:1200px">
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link to="/noticia"
                    ><v-img style="height:400px" :src="blocourls[0]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link to="/noticia"
                    ><v-img style="height:400px" :src="blocourls[1]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link to="/noticia"
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
                  <nuxt-link to="/noticia"
                    ><v-img style="height:600px" :src="blocourls[3]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:600px">
                  <nuxt-link to="/noticia"
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
                  <nuxt-link to="/noticia"
                    ><v-img style="height:400px" :src="blocourls[5]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link to="/noticia"
                    ><v-img style="height:400px" :src="blocourls[6]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <nuxt-link to="/noticia"
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
                  <nuxt-link to="/noticia"
                    ><v-img style="height:300px" :src="blocourls[8]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link to="/noticia"
                    ><v-img style="height:300px" :src="blocourls[9]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link to="/noticia"
                    ><v-img style="height:300px" :src="blocourls[2]"></v-img
                  ></nuxt-link>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <nuxt-link to="/noticia"
                    ><v-img style="height:300px" :src="blocourls[3]"></v-img
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
    array: []
  }),
  created: function() {
    const self = this
    console.log('------------------created-----------------')
    console.log(self.results)
    axios
      .get(
        'https://api.unsplash.com/search/photos/?page=1;query=girl;orientation=landscape;client_id=2ebf903d65d58846dba610108cbf428043756525989c37bfd1121174ff28a339'
      )
      .then(function(response) {
        self.array.push(response)
        console.log('------------------axios response-----------------')
        console.log(self.array)
        console.log('------------------axios response-----------------')
        for (const index in self.array[0].data.results) {
          // don't actually do this
          self.blocourls.push(self.array[0].data.results[index].urls.regular)
        }
        console.log(self.bloco)
      })
      .catch(function(error) {
        console.log(error)
      })
  }
}
</script>
<style media="screen">
a {
  padding: 0;
  margin: 0;
}
</style>
