<template lang="pug">
  div(class="c-content__center")
    m-page-title Contact
    div(class="lead enter-fade-up enter-delay-1")
      p Think we can make great things together?
      span
        a(href="matheusgomes062@gmail.com") Let's get in touch!
    div(class="enter-fade-up enter-delay-2")
    m-social
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'
import MPageTitle from '~/components/MPageTitle.vue'
import MSocial from '~/components/MSocial.vue'

export default defineComponent({
  name: 'Contact',

  components: {
    MSocial,
    MPageTitle
  },

  head() {
    return {
      title: 'Contact'
    }
  }
})
</script>
