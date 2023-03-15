<template>
    <div>
        <input @keyup.enter="onInput" placeholder="City" />
    </div>
</template>

<script>
export default {
    name: 'CityInput',
    methods: {
        onInput: function(event) {
            this.$emit('citySubmit', event.target.value)
        }
    }
}
</script>

<style scoped>
input {
    margin-top: 5%;
    width: 80%;
    height: 30px;
    border-radius: 10px;
    box-shadow: 10px 5px 5px;
    text-align: center;
}
</style>