<template>
  <div class="container main">
    <div class="row">
      <div class="col">
        <ul class="list-group">
          <li class="list-group-item">{{ renderItem() }}</li>
        </ul>
      </div>
      <div class="col"><Form :handleSubmit="handleSubmit" /></div>
    </div>
  </div>
</template>

<script>
import Form from './Form.vue'
export default {
  name: 'Main',
  components: {
    Form,
  },
  props: {
    item: String,
    handleSubmit: Function,
  },
  methods: {
    renderItem() {
      return this.item ? this.item : 'Clicked items will come here'
    },
  },
}
</script>
