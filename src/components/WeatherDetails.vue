<template>
    <div v-if="weather != null" class="details">
        <img :src="weather.current.weather_icons[0]"/>
        <div class="time">{{weather.current.observation_time}}</div>
        <div class="city">{{weather.location.name}} {{weather.location.region}}</div>
        <div class="temp">{{weather.current.temperature}} F</div>
        <div class="desc">{{weather.current.weather_descriptions[0]}}</div>
    </div>
    <div v-else class="details">

    </div>
</template>

<script>
export default {
    name: 'WeatherDetails',
    props: ['weather']
}
</script>

<style scoped>
.details {
    margin: 15px;
    height: 80%;
    background-color: #c0c0c0;
    border-radius: 10px;
    box-shadow: 8px 5px 5px;
    opacity: 50%;
}

.time {
    margin: 2%;
    font-size: x-large;
}

.city {
    margin: 2%;
    font-size: x-large;
}

.temp {
    margin: 2%;
    font-size: xx-large;
}

.desc {
    margin: 2%;
    font-size: x-large;
}

img {
    margin-top: 15%;
}
</style>