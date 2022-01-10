<template>
  <div>
    <h1>{{ $route.params.id }}</h1>
    <button @click="$router.push('/products')">back</button>
  </div>
</template>