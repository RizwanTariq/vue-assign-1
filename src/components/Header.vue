<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary mb-5">
    <div class="container-fluid">
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarColor01"
        aria-controls="navbarColor01"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarColor01">
        <ul class="navbar-nav me-auto">
          <li v-for="(item, index) in list" :key="index" class="nav-item">
            <button @click="handleClick(item)" class="btn nav-link">
              {{ item }}
            </button>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Header',
  props: {
    list: Array,
    item: String,
    handleClick: Function,
  },
}
</script>
