<template>
  
</template>
<script lang="ts">
import {ref} from 'vue'
export default {
  name:'z-switch',
  props: {
    value:Boolean
  },
  setup(props, context) {
    const toggle = () => {
      context.emit('update:value', !props.value)
    }
    return {
      toggle
    }
  }
}
</script>
<style lang="scss">


</style>