<template>
  <div class="c-content">
    <slot />
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'
import MNavigation from '~/components/MNavigation.vue'

export default defineComponent({
  name: 'SContent',

  components: {
    MNavigation
  }
})
</script>
