<template>
  <div class="grid md:grid-cols-2 gap-4">
      <!-- Box 1 -->
      <div class="shadow-md bg-blue-100 p-10 text-center rounded">
          <h3 class="text-3xl text-blue-900 font-bold mb-4">Cases</h3>
          <div class="text-2xl mb-4">
              <span class="font-bold">New:</span>
              {{addCommas(stats.NewConfirmed)}} 
          </div>
          <div class="text-2xl mb-4">
              <span class="font-bold">Total:</span>
              {{addCommas(stats.TotalConfirmed)}} 
          </div>
      </div>
      <!-- Box 2 -->
       <div class="shadow-md bg-blue-200 p-10 text-center rounded">
          <h3 class="text-3xl text-blue-900 font-bold mb-4">Deaths </h3>
          <div class="text-2xl mb-4">
              <span class="font-bold">New:</span>
              {{addCommas(stats.NewDeaths)}} 
          </div>
          <div class="text-2xl mb-4">
              <span class="font-bold">Total:</span>
              {{addCommas(stats.TotalDeaths)}} 
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'DataBoxes',
    props: ['stats'],
    methods: {
        addCommas(num){
            return num.toString()
          .replace(/\B(?=(\d{3})+(?!\d))/g, ',');
        }
    }
}
</script>

<style>

</style>