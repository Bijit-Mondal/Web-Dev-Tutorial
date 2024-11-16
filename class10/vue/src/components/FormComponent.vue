<template>
  <div class="form-container">
    <h2>Sample Form</h2>
    <form @submit.prevent="handleSubmit">
      <InputComponent id="name" label="Name" type="text" v-model="formData.name" />
      <InputComponent id="email" label="Email" type="email" v-model="formData.email" />
      
      <SelectComponent 
        id="age" 
        label="Age" 
        v-model="formData.age" 
        :options="[
          { value: '18-24', text: '18-24' },
          { value: '25-34', text: '25-34' },
          { value: '35-44', text: '35-44' },
          { value: '45+', text: '45+' }
        ]" 
      />
      
      <CheckboxComponent 
        id="subscribe" 
        label="Subscribe to Newsletter" 
        type="checkbox" 
        v-model="formData.subscribe" 
      />
      
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
import InputComponent from './InputComponent.vue'
import SelectComponent from './SelectComponent.vue'
import CheckboxComponent from './CheckboxComponent.vue'

export default {
  components: {
    InputComponent,
    SelectComponent,
    CheckboxComponent
  },
  data() {
    return {
      formData: {
        name: '',
        email: '',
        age: '',
        subscribe: false
      }
    }
  },
  methods: {
    handleSubmit() {
      this.$emit('form-submitted', this.formData)
    }
  }
}
</script>

<style>
/* Style the form container */
.form-container {
  width: 50%;
  margin: 40px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
</style>
