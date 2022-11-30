<template>
  <div id='errorText' class="errorText" v-if="hasError">
    <p>We didn't find the city {{ searchQuery }}, try again with another one</p>
  </div>
</template>


<script>
// import CitySearchbar from './components/CitySearchbar.vue'

export default {
name: 'ErrorMessage',
// components: {
//   CitySearchbar,
// },

props: ['onSearch'],
data: () => {
  return {
    searchQuery: '',
    hasError: false,
  }
}, 
}
