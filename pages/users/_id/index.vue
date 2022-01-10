<template>
  <div>
    <h1>{{ $route.params.id }}</h1>
    <button @click="showUsers">back</button>
  </div>
</template>

<script>
export default {
  validate(data) {
    return /^-?\d+$/.test(data.params.id)
  },
  methods: {
    showUsers() {
      this.$router.push('/users')
    }
  },
  layout: 'users'
}
</script>