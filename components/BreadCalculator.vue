<template>
  <div class="dark:text-gray-100 flex flex-col max-w-sm w-64 text-left rounded overflow-hidden shadow-lg">
    <div class="px-6 py-4">
      <div class="font-bold text-xl mb-2 text-center mb-3">Kalkulator</div>
      <label for="weight">Moka (g)</label>
      <input type="number" name="weight" v-model="weight" class="dark:text-gray-800 bg-white focus:outline-none focus:shadow-outline border border-gray-300 rounded-lg py-2 px-4 block w-full appearance-none leading-normal dark:bg-indigo-100 mt-2 mb-3" min="0">
      <label for="hidration" class="">Hidracija (%)</label>
      <input type="number" name="hidration" v-model="hidration" class="dark:text-gray-800 bg-white focus:outline-none focus:shadow-outline border border-gray-300 rounded-lg py-2 px-4 block w-full appearance-none leading-normal mt-2 dark:bg-indigo-100" min="0" max="100">
      <p class="mt-3"> Voda (g): {{water}}</p>
      <p class="mt-3"> Sol (g): {{salt}}</p>
      <p class="mt-3"> Suhi kvas (g): {{yeast}}</p>
    </div>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      weight: 1000,
      hidration: 72,
    }
  },
  computed: {
    water() {
      return (Math.round(this.hidration/10 * this.weight) / 10).toFixed(1);
    },
    salt() {
      return (Math.round(0.2 * this.weight) / 10).toFixed(1);
    },
    yeast() {
      return (Math.round(0.04 * this.weight) / 10).toFixed(1);
    },
  }
}
</script>

<style>

</style>