<template>
  <div class="display">
    <WeatherDetails :weather="weather"/>
    <CityInput @citySubmit="onCitySubmit"/>
  </div>
</template>

<script>
import CityInput from "./CityInput.vue";
import WeatherDetails from "./WeatherDetails.vue";
import axios from "axios";
const ACCESS_KEY = 'fdc1cadb7e791f4a059290c56b4b68a5';

export default {
  name: 'HelloWorld',
  components: {
    WeatherDetails,
    CityInput
  },
  data() {
        return { weather: null};
  },
  methods: {
    onCitySubmit(city) {
      axios.get(`http://api.weatherstack.com/current?access_key=${ACCESS_KEY}&query=${city}&units=f`)
      .then(response => {
                this.weather = response.data;
            })
    }
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
  background-color: #5d5b9f;
  text-align: center;
  opacity: 90%;
}
</style>
