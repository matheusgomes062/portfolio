<template lang="pug">
  div(class="c-content__center")
    m-page-title About
    div(class="lead enter-fade-up enter-delay-1")
      p Hi, I'm Matheus Gomes, 23 years old, living in and in love with São José dos Campos.
    div(class="enter-fade-up enter-delay-2")
      p 
      | After finishing High School I decided to start a Bachaleor's degree in Science and Technology at UNIFESP and later on become a full-time digital designer and developer. End of 2018, I began working as an #[strong Full Stack Developer Intern] at <a href="https://agrotools.com.br/">Agrotools</a>, a Brazilian-based agtech startup.
      p
      | In the begning of 2020 I was promoted to #[strong Mid-level Full Stack Developer] in the same company. Later on I started working as a Back-end Developer for <a href="https://animaeducacao.com.br/">Ânima Educação</a>, one of Brazil's biggest education companies. Later that year I joined Pixfy, a software house that a friend of mine build from the ground up with a shared love of great design and technology. There I worked as a #[strong Lead Front-End Developer] until the end. Then in 2021 I also worked as a #[strong Full Stack Developer] at <a href="https://spread.com.br/">Spread Tecnologia</a> one of Brazil biggest software houses and consulting companies.
      
      p
      | Now, in 2021 I wrote a <a href="https://github.com/matheusgomes062/guia-markdown/blob/master/Markdown%20LIVRO.md">book</a> and started my own company, the PWR Pixel company, to provide #[strong quality Front-End] services to startups and other companies. Always aiming at delivering #[strong value and high perfomance applications]🚀.

      figure
        img(src="https://images.unsplash.com/photo-1592609931095-54a2168ae893?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80" data-image="390" style="width:800px; height:250px; object-fit:cover; object-position: 100% 80%;")
      
      p
      | Apart from design and code, I love playing guitar, videogames, going to the gym or watching a movie. I also love coffee, so we should definitely grab one together. ☕️
    m-social
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'
import MPageTitle from '~/components/MPageTitle.vue'
import MSocial from '~/components/MSocial.vue'

export default defineComponent({
  name: 'About',

  components: {
    MSocial,
    MPageTitle
  },

  head() {
    return {
      title: 'About'
    }
  },
})
</script>
