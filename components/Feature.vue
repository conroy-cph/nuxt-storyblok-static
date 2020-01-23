<template>
  <div v-editable="blok" class="column feature">
    {{blok.name}}
  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>

<style scoped>
.feature {
    border: 1px solid grey;
    box-shadow: 1px 1px rgba(0, 0, 0, 0.4);
}
</style>