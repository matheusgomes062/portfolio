<template>
  <div class="c-content__center">
    <s-page-title>{{ page.title }}</s-page-title>
    <div class="lead enter-fade-up enter-delay-1" v-html="page.introduction" />
    <s-services :services="services" />
    <s-social />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'
import SPageTitle from '~/components/SPageTitle.vue'
import SSocial from '~/components/SSocial.vue'
import SServices from '~/components/SServices.vue'

export default defineComponent({
  name: 'Index',

  components: {
    SSocial,
    SPageTitle,
    SServices
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
