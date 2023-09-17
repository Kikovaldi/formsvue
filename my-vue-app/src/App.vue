<script>
import { createApp } from "vue";

export default {
  name: "App",
  components: {},
  data() {
    return {
      city: "Barcelona",
      cities: [],
    };
  },

  methods: {
    addCity() {
      this.cities.push(this.city);
      this.city = "";
      console.log (this.cities)
      return this.cities;
    },
  },
  computed: {
    welcomeSentence(){
      return `my city is ${this.city}`
    }
  }
};
</script>

<template>
<h1>{{ welcomeSentence }}</h1>
  <form action="">
    <input type="text" name="city" v-model="city" /> 
    <button @click.prevent="addCity">Submit</button>
  </form>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
