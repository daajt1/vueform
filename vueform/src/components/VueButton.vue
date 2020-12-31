<template>
    <div id="app" class="ui container">
<h2 class="ui header">What's your favorite tee</h2>

<button @click="onButtonClick"
name="button-tee"
value="RedTea"
class="ui button">Red Tea</button>
<button @click="onButtonClick"
name="button-tee"
value="GreenTee"
class="ui button">Green Tea</button>
<button @click="onButtonClick"
name="button-tee"
value="Blacktea"
class="ui button">Black Tea</button>
<button @click="onButtonClick"
name="button-jacket"
value="Yellow Tea"
class="ui button">Yellow Tea</button>
</div>

</template>

<script>


export default {

methods: {
onButtonClick(evt) {
const button = evt.target;
console.log(`The user clicked ${button.name}: ${button.value}`);
}
}
}
</script>

<style scoped>

</style>