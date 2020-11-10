<template>
  <form @submit.prevent="onSubmit">
    <label>
      <input v-model="text" type="text" placeholder="Search Jokes...">
    </label>
    <input type="submit" value="Search Jokes">
  </form>
</template>

<script>
export default {
  name: 'SearchJokes',
  data () {
    return {
      text: ''
    }
  },
  methods: {
    onSubmit () {
      this.$emit('search-text', this.text)
      this.text = ''
    }
  }
}
</script>

<style scoped>

</style>
