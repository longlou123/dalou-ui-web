<demo>示例代码</demo>
<template>
  <div>
    <z-switch v-model:value="check"></z-switch>
  </div>
</template>

<script>
export default {
  name: 'switch-demo',
  components: {},
  data (){
    return {
      check: true
    }
  }
}
</script>
