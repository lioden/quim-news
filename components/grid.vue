<template>
  <div>
    <v-container fluid grid-list>
      <v-layout row wrap>
        <v-flex d-flex xs12 sm6 md4 style="height:1200px">
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12 style="height:400px">
                  <v-img style="object-fit: contain;" :src="imagens[7]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <v-img style="object-fit: contain" :src="imagens[6]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <v-img style="object-fit: contain" :src="imagens[5]"></v-img>
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
                  <v-img style="object-fit: contain" :src="imagens[6]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:600px">
                  <v-img style="object-fit: contain" :src="imagens[5]"></v-img>
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
                  <v-img style="object-fit: contain;" :src="imagens[1]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <v-img style="object-fit: contain" :src="imagens[2]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:400px">
                  <v-img style="object-fit: contain" :src="imagens[3]"></v-img>
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
                  <v-img style="object-fit: fill" :src="imagens[4]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <v-img style="object-fit: fill" :src="imagens[5]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <v-img style="object-fit: fill" :src="imagens[7]"></v-img>
                </v-flex>
                <v-flex d-flex xs12 style="height:300px">
                  <v-img style="object-fit: fill" :src="imagens[6]"></v-img>
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
export default {
  data: () => ({
    imagens: [
      'https://images.unsplash.com/photo-1553969546-6f7388a7e07c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60',
      'https://images.unsplash.com/photo-1554197324-9a1c73a755ac?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1349&q=80',
      'https://images.unsplash.com/photo-1553969488-312435bebbf4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60',
      'https://images.unsplash.com/photo-1554196222-3464352db975?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80',
      'https://images.unsplash.com/photo-1553974021-c410ec0336bf?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80',
      'https://images.unsplash.com/photo-1553971371-1ff3607279c0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1940&q=80',
      'https://images.unsplash.com/photo-1524260855046-f743b3cdad07?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1401&q=80',
      'https://images.unsplash.com/photo-1523712999610-f77fbcfc3843?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'
    ],
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`
  })
}
</script>
