<template>
  <div>
    <p>This is an article page</p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  mounted: function() {
    const self = this
    axios
      .post(
        'http://gateway.loba.pt:3001/rest/pagecontent?lang=' +
          self.$route.params.lang +
          '&route=' +
          self.$route.params.article
      )
      .then(response => {
        console.log(response)
      })
  }
}
</script>

<style lang="css" scoped></style>
