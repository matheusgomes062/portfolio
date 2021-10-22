<template lang="pug">
  div(class="c-content__center")
    m-page-title Matheus Gomes
    div(class="lead enter-fade-up enter-delay-1")
      p Freelance #[strong front-end developer] and #[strong writer]. Dreams in HTML, CSS and Javascript, lives in São José dos Campos, Brazil. Helps other people build digital products.
    m-services(:services="services")
    m-social
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'
import MPageTitle from '~/components/MPageTitle.vue'
import MSocial from '~/components/MSocial.vue'
import MServices from '~/components/MServices.vue'

export default defineComponent({
  name: 'Index',

  components: {
    MSocial,
    MPageTitle,
    MServices
  },

  head() {
    return {
      title: 'Home'
    }
  },

  async asyncData() {
    const pages = await (
      await fetch(
        'https://portfolio.simonwuyts.eu/portfolio/items/pages?fields=*.*'
      )
    ).json()
    const services = await (
      await fetch(
        'https://portfolio.simonwuyts.eu/portfolio/items/services?fields=*.*'
      )
    ).json()

    return {
      services: services.data,
      page: pages.data.filter((page: any) => page.slug === 'home')[0]
    }
  }
})
</script>
