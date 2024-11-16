<template>
  <div class="output-container">
    <h2>Form Output</h2>
    <p>{{ output }}</p>
  </div>
</template>

<script>
export default {
  props: {
    output: Object
  }
}
</script>

<style>
/* Style the output container */
.output-container {
  width: 50%;
  margin: 40px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
</style>
