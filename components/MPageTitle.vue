<template lang="pug">
  h1(class="c-title enter-fade-up")
    div(class="c-title__border" aria-hidden="true")
      span(class="c-title__inner")
        slot
    div(class="c-title__text")
      span
        slot
</template>

<script lang="ts">
export default {
  name: 'MPageTitle'
}
</script>
