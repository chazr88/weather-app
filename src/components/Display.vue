<template>
  <div class="display">
    <WeatherDetails/>
    <CityInput/>
  </div>
</template>

<script>
import CityInput from "./CityInput.vue";
import WeatherDetails from "./WeatherDetails.vue";

export default {
  name: 'HelloWorld',
  components: {
    WeatherDetails,
    CityInput
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.display {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  height: 600px;
  width: 500px;
  border-radius: 10px;
  background-color: rgb(197, 196, 196);
  text-align: center;
  opacity: 90%;
}
</style>
