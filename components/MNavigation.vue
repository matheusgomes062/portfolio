<template lang="pug">
  nav(class="c-navigation")
    nuxt-link(class="c-navigation__logo" to="/")
      s-logo
      span(class="sr-only") Home
    div(class="c-navigation__left")
      nuxt-link(
        to="/"
        class="c-navigation__item"
        active-class="c-navigation__item--active"
        exact) Home
      nuxt-link(
        to="/about"
        class="c-navigation__item"
        active-class="c-navigation__item--active"
        exact) About
      //- nuxt-link(
      //-   to="/articles"
      //-   class="c-navigation__item"
      //-   active-class="c-navigation__item--active") Articles
      nuxt-link(
        to="/contact"
        class="c-navigation__item"
        active-class="c-navigation__item--active"
        exact) Contact
</template>

<script lang="ts">
import { defineComponent, computed } from '@vue/composition-api'
import SLogo from '~/components/SLogo.vue'

export default defineComponent({
  name: 'MNavigation',

  components: {
    SLogo
  },

  setup() {
    const nlPath = computed(() => `/nl/`)
    const enPath = computed(() => `/`)

    return {
      nlPath,
      enPath
    }
  }
})
</script>
