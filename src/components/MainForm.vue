<template>
  <fish-form>
    <h1>Title</h1>
    <fish-field label="Text input" span="24">
      <fish-input v-model="textInput"></fish-input>
    </fish-field>
    <fish-field label="Number input" span="24">
      <fish-input-number v-model="numInput"></fish-input-number>
    </fish-field>
    <fish-field label="Number input" span="24">
      <fish-input-number v-model="numInput"></fish-input-number>
    </fish-field>
    <div class="submit-wrapper">
      <fish-button type="positive" size="large" @click="calculateResults">Submit</fish-button>
    </div>
    <fish-field label="Result" span="24" v-if="result || result === 0">
      <h2>{{ result }}</h2>
    </fish-field>
  </fish-form>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      textInput: 'Textfield',
      numInput: 0.42,
      result: null
    }
  },
  methods: {
    calculateResults() {
      this.result = this.numInput * 8;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  form {
    padding: 20px;
    max-width: 1000px;
    min-width: 1000px;
    margin: 0 auto;

    .submit-wrapper {
      text-align: center;
    }

    h1 {
      text-align: center;
    }
  }

</style>
