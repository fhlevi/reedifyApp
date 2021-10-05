<template>
    <v-app-bar
      :class="{'reedify-header px-14': true, 'header-bg': isBackground}"
      fixed
      app
      flat
    >
      <img :src="require('Assets/img/icons/reedify.png')" class="reedify-header-image" alt="logo header" />
      <v-toolbar-title class="header-title">Reedify Finance</v-toolbar-title>
    </v-app-bar>
</template>

<script>
export default {
    name: 'AppHeader',
    data() {
      return {
          isBackground: false
      }
    },
    mounted(){
        window.addEventListener('scroll', this.onScroll)
    },
    beforeDestroy(){
        window.removeEventListener('scroll', this.onScroll)
    },
    methods: {
        onScroll() {
            const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop

            if(currentScrollPosition < 0) {
              return
            }

            this.isBackground = currentScrollPosition > 0
        },
    }
}
</script>