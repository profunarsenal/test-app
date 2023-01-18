<template lang="pug">
  button(@click="share") Facebook
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
    name: 'Index',

    head () {
        return {
            meta: [
            { property: 'og:type', content: 'website' },
            { property: 'og:title', content: 'Title' },
            { property: 'og:description', content: 'test' },
            { property: 'og:image', content: 'https://cdn.freelance.ru/images/att/1693618_900_600.png' },
            { property: 'og:site_name', content: 'site' },
            { property: 'og:url', content: 'https://fix-price.com/' },
          ]
        }
    },

    methods: {
      share() {
        window.open(
                'https://www.facebook.com/share.php?u=' + `${location.protocol}//${location.host}${this.$route.path}`,
                'share',
                'left=-50%,top=-50%,width=600,height=400',
            );
      }
    }
})
</script>

<style lang="sass" scoped>
</style>
