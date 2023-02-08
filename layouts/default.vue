<template>
  <v-app>
    <div v-if="announce" class="announce">
      <v-container>
        <v-row class="d-flex align-center justify-center">
          <span>Figma connects everyone in the design process</span>
          <v-btn icon v-on:click="close">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-row>
      </v-container>
    </div>

 
 
    <v-main>
      <v-row class="d-flex justify-space-between" style="padding: 0 30px; margin-top:20px;">
        <a href="/"><FigmaLogo /></a>
        <div><a href="/pricing">Pricing</a></div>
      </v-row>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

  </v-app>
</template>

<script>
  export default {
    name: 'DefaultLayout',
    data () {
      return {
        announce: true,
        items: [
          {
            icon: 'mdi-apps',
            title: 'Welcome',
            to: '/'
          },
          {
            icon: 'mdi-chart-bubble',
            title: 'Inspire',
            to: '/inspire'
          }
        ],
        title: 'Vuetify.js'
      }
    },
    methods:{
      close() {
        this.announce = false
      },

    }
  }
</script>
<style>
  .announce{
    background: rosybrown;
  }

</style>