<template>
  <div class="container">
    <div class="">
      <button
        @click="toggle"
        class="absolute top-0 bg-green-500 hover:bg-green-700 text-white py-1 px-2 md:py-2 md:px-4 rounded mt-5 text-xs md:text-md l-toggle-button"
      >{{$colorMode.value == 'light' ? 'Lights off' : 'Lights on'}}</button>
      <h1 class="title dark:text-gray-100 mt-5">Primož Kerin</h1>
      <div class="links">
        <nuxt-link to="/blog-post-bread" class="text-green-500 border-solid border-b-2 py-2 px-2 mr-2 border-green-500">Kruh kalkulator</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  methods: {
    toggle() {
      this.$colorMode.value =
        this.$colorMode.value == 'light' ? 'dark' : 'light'
    }
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.l-toggle-button {
  right: 50px;
}
</style>
