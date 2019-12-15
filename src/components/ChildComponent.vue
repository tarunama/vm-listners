<template>
  <button
    @click="$emit('click')"
    @mouseover="$emit('mouseover')"
  >
    button
  </button>
</template>

<script>
export default {
    name: 'ChildComponent'
}
</script>