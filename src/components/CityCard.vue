<template>
  <div id="components-demo">
    <div id="cityDiv" class="cityHistory-div" v-for="(item, index) in cityHistory.slice().reverse()" v-bind:key="index">
      <div class="cityHistory-box">
        <h2 class="cityHistory-title">{{ item.name }}</h2>
        <h3 class="cityHistory-temp">{{ item.temp }}°c</h3>
        <p class="cityHistory-weather">{{ item.weather }}</p>
      </div>
      <div class="text-center">
      </div>
      <v-btn class="mx-2" dark small v-on:click="remove(index)">
        <i class='bx bx-trash'></i>
        <span>Delete </span>
      </v-btn>
    </div>
  </div>
</template>


<script>
export default {
  name: 'CityCard',
  props: ['cityHistory', 'name',
    'temp',
    'weather'
  ],
  data: () => {
    return {
      hasError: false,
    }
  },
  methods: {
     remove() {
      let removeCity = document.getElementById("cityDiv");
      removeCity.remove();
      this.hasError = true;
      return;
    },

  },
}

</script>

