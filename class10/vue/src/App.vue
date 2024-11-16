<template>
  <div>
    <FormComponent @form-submitted="handleFormSubmission" />
    <OutputComponent :output="formOutput" />
  </div>
</template>

<script>
import FormComponent from './components/FormComponent.vue'
import OutputComponent from './components/OutputComponent.vue'

export default {
  components: {
    FormComponent,
    OutputComponent
  },
  data() {
    return {
      formOutput: {}
    }
  },
  methods: {
    handleFormSubmission(formData) {
      this.formOutput = formData
    }
  }
}
</script>
