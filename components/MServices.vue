<template lang="pug">
  div(class="c-services")
    div(
      class="c-service"
      :class="`enter-fade-up enter-delay-${index + 2}`"
      v-for="(service, index) in services")
    
      div(class="c-service__icon")
        img(
          class="c-service__image"
          :src="service.image.data.url"
          :alt="service.title")
      div(class="c-service__description")
        h2 {{ service.title }}
        div(v-html="service.description")
</template>

<script lang="ts">
export default {
  name: 'MServices',
  data() {
    return {
      services: [
        {
          title: 'Web app design',
          description: `Whether it's designing a new product or refreshing the design of an existing application, I'm happy to help making your project beautiful and easy to use.`,
          image: {
            data: {
              url:
                'https://s3.eu-west-3.amazonaws.com/simonwuyts-portfolio/bb43f04a-8d25-4767-8d69-ffdf596fe545.svg'
            }
          }
        },
        {
          title: 'Front-end development',
          description: `Modern browsers offer a lot of possibilities but also demand for a specialized approach. I translate designs to production ready HTML, CSS and Javascript. <a class="link-vue" href='https://www.vuejs.org/'/>Vue.js</a> and <a class="link-nuxt" href='https://nuxtjs.org/'/>Nuxt</a> complete my front-end stack.`,
          image: {
            data: {
              url:
                'https://s3.eu-west-3.amazonaws.com/simonwuyts-portfolio/a471ed3d-cd54-47d2-a549-9b12698746a7.svg'
            }
          }
        }
      ]
    }
  },
  methods: {}
}
</script>
