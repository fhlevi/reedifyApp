<template>
  <v-app dark>
    <app-header></app-header>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <app-footer></app-footer>
  </v-app>
</template>

<script>
export default {
  components: {
    'app-header': () => import('@/components/template/AppHeader.vue'),
    'app-footer': () => import('@/components/template/AppFooter.vue')
  },
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
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
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
