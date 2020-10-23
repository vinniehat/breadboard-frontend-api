<template>
  <div class="single-led">
    <h1 >LED Status: {{isLEDOn}}</h1>
    <button @click="toggleLED">Toggle LED</button>
  </div>
</template>

<script>
const axios = require("axios");
export default {
  name: "SingleLED",
  data() {
    return {
      isLEDOn: "off"
    }
  },
  methods: {
    toggleLED() {
      if (this.isLEDOn === "off") {
        axios(`${this.$store.state.API_URL}/led/on`, {
          method: "POST",
        })
        this.isLEDOn = "on";
      } else if (this.isLEDOn === "on") {
        axios(`${this.$store.state.API_URL}/led/off`, {
          method: "POST",
        })
        this.isLEDOn = "off";
      }
    }
  }
}
</script>

<style scoped>
.single-led {
  text-align: left;
  margin-left: 15px;
  border: #2c3e50 4px solid;
  display: inline-grid;
  padding: 15px;
}
</style>