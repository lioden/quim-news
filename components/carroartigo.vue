<template>
  <v-carousel hide-delimiters>
    <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src">
      <div class="overlay"></div>
      <div class="centrado">
        <p>{{ item.text }}</p>
      </div>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src:
            'https://images.unsplash.com/photo-1452857297128-d9c29adba80b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1267&q=80'
        },
        {
          src:
            'https://www.heraldry-wiki.com/arms/websites/Portugal/www.fisicohomepage.hpg.ig.com.br/images/VAC-codal.gif'
        },
        {
          src:
            'https://kashmirlife.net/wp-content/uploads/2016/10/Wadwan-fire2.jpg'
        },
        {
          src:
            'https://img.maximummedia.ie/joe_ie/eyJkYXRhIjoie1widXJsXCI6XCJodHRwOlxcXC9cXFwvbWVkaWEtam9lLm1heGltdW1tZWRpYS5pZS5zMy5hbWF6b25hd3MuY29tXFxcL3dwLWNvbnRlbnRcXFwvdXBsb2Fkc1xcXC8yMDE1XFxcLzExXFxcLzIzMTc1OTE4XFxcL0NyeWluZy5qcGdcIixcIndpZHRoXCI6NzY3LFwiaGVpZ2h0XCI6NDMxLFwiZGVmYXVsdFwiOlwiaHR0cHM6XFxcL1xcXC93d3cuam9lLmllXFxcL2Fzc2V0c1xcXC9pbWFnZXNcXFwvam9lXFxcL25vLWltYWdlLnBuZz92PTIyXCIsXCJvcHRpb25zXCI6W119IiwiaGFzaCI6ImY0MjE0ZmQyNTc3Nzg3MjYxN2QyNDRiMjc0YjBiNWM1OTMzYjAzYjEifQ==/crying.jpg'
        }
      ]
    }
  }
}
</script>

<style>
.centrado {
  position: absolute;
  left: 10%;
  right: 10%;
  top: 50%;
  color: #fff;
  text-align: center;
  display: inline-block;
  margin: 0 auto;
  z-index: 3;
}

.overlay {
  position: absolute; /* Sit on top of the page content */
  width: 100%; /* Full width (cover the whole page) */
  height: 100%; /* Full height (cover the whole page) */
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.1); /* Black background with opacity */
  z-index: 2; /* Specify a stack order in case you're using a different order for other elements */
}
</style>
