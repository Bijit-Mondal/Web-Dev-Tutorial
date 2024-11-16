<template>
  <div>
    <label :for="id">{{ label }}</label>
    <input :type="type" :id="id" :value="value" @input="$emit('input', $event.target.value)" required>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    label: String,
    type: String,
    value: String
  }
}
</script>

<style>
/* Style the input field */
input {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
</style>
