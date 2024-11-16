<template>
  <div>
    <label :for="id">{{ label }}</label>
    <input :type="type" :id="id" :checked="value" @change="$emit('input', $event.target.checked)" required>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    label: String,
    type: String,
    value: Boolean
  }
}
</script>

<style>
/* Style the checkbox field */
input[type="checkbox"] {
  margin-right: 10px;
}
</style>
