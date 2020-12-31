<template>
 <form @submit="submitForm" class="ui form">
<div class="field">
<label>New Item</label>
<input v-model="fields.newItem" type="text" placeholder="Add an item!" />
<span style="color: red">{{ fieldErrors.newItem }}</span>
</div>
<!-- Email Field -->
<div class="field">
<label>Email</label>
<input v-model="fields.email" type="text" placeholder="What's your email?" />
<span style="color: red">{{ fieldErrors.email }}</span>
</div>
<!-- Urgency Field -->
<div class="field">
<label>Urgency</label>
<select v-model="fields.urgency" class="ui fluid search dropdown">
<option disabled value="">Please select one</option>
<option>Nonessential</option>
<option>Moderate</option>
<option>Urgent</option>
</select>
<span style="color: red">{{ fieldErrors.urgency }}</span>
</div>
<!-- Terms and conditions checkbox -->
<div class="field">
<div class="ui checkbox">
<input v-model="fields.termsAndConditions" type="checkbox" />
<label>I accept the terms and conditions</label>
<span style="color: red">{{ fieldErrors.termsAndConditions }}</span>
</div>
</div>
<button class="ui button">Submit</button>
</form>
</template>

<script>
export default {
  name: 'VueForm',
 data() {
return {
fields: {
newItem: '',
email: '',
urgency: '',
termsAndConditions: false
},
fieldErrors: {
newItem: undefined,
email: undefined,
urgency: undefined,
termsAndConditions: undefined
},

items: []
}
 },
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
