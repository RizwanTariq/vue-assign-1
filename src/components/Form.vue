<template>
  <form @submit.prevent="onSubmit()">
    <fieldset className="m-10">
      <div className="form-group">
        <label htmlFor="text" className="form-label mt-4"> Text </label>
        <input
          type="text"
          v-model="text"
          aria-describedby="text"
          className="form-control mb-3"
          placeholder="Enter Text"
          required
        />
      </div>
      <button type="submit" className="btn btn-primary">Submit</button>
    </fieldset>
  </form>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      text: '',
    }
  },
  props: {
    handleSubmit: Function,
  },
  methods: {
    onSubmit() {
      this.handleSubmit(this.text)
      this.text = ''
    },
  },
}
</script>
