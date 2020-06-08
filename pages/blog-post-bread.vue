<template>
  <div class="container">
    <div class="flex flex-col">
      <nuxt-link to="/" class="block text-green-500 border-solid border-b-2 py-2 px-2 border-green-500 mt-8 w-16 self-center">
        Home
      </nuxt-link>
      <button
        @click="toggle"
        class="absolute top-0 bg-green-500 hover:bg-green-700 text-white py-1 px-2 md:py-2 md:px-4 rounded mt-5 text-xs md:text-md l-toggle-button"
      >{{$colorMode.value == 'light' ? 'Lights off' : 'Lights on'}}</button>
      <h1 class="b-title dark:text-gray-100 mt-5">Kalkulator sestavin za kruh</h1>
      <h2 class="b-subtitle dark:text-gray-300 mt-1">Kruh hočem rezat</h2>
      <div class="content max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero reprehenderit inventore, a repellendus error deserunt quasi nesciunt repudiandae porro quidem sapiente doloribus magni veritatis, soluta rerum sequi eius beatae adipisci?</p>
      </div>
      <div class="flex justify-center">
        <bread-calculator />
      </div>

      <h2 class="subtitle mt-5 dark:text-gray-300">Recept</h2>
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eveniet ex enim quo illum voluptas, culpa quisquam. Harum, delectus animi? At aspernatur modi soluta nesciunt debitis vero voluptas distinctio obcaecati voluptate!
      </p>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import BreadCalculator from '~/components/BreadCalculator.vue'

export default {
  components: {
    Logo,
    BreadCalculator,
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
  /* @apply min-h-screen flex justify-center text-center mx-auto; */
}

.b-title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 42px;
  color: #35495e;
  letter-spacing: 1px;
}

.b-subtitle {
  font-weight: 300;
  font-size: 28px;
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
