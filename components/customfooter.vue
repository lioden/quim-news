<template>
  <v-footer dark height="auto">
    <v-card class="flex" flat tile>
      <v-card-title class="grey darken-2">
        <v-card-text class="white--text pt-0 text-xs-center">
          Made with ❤ by Senhor Joaquim
        </v-card-text>
      </v-card-title>

      <v-card-actions class="grey darken-3 justify-center">
        &copy;2019 — <strong>LOBA</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      'fab fa-facebook',
      'fab fa-twitter',
      'fab fa-google-plus',
      'fab fa-linkedin',
      'fab fa-instagram'
    ]
  })
}
</script>
