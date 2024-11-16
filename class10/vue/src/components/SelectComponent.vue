<template>
  <div>
    <label :for="id">{{ label }}</label>
    <select :id="id" :value="value" @change="$emit('input', $event.target.value)" required>
      <option v-for="(option, index) in options" :key="index" :value="option.value">{{ option.text }}</option>
    </select>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    label: String,
    value: String,
    options: Array
  }
}
</script>

<style>
/* Style the select field */
select {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
</style>
