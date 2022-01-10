<template>
  <div>
    <input type="number" v-model.number="id">
    <button @click="showUser">Load user</button>
    <NuxtChild />
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: Number
    }
  },
  methods: {
    showUser() {
      if (typeof this.id === 'number') {
        this.$router.push(`/users/${this.id}`)
      }
    }
  },
  layout: 'users'
}
</script>
