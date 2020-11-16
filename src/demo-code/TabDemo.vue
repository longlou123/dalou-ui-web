<demo>示例代码</demo>
<template>
  <z-tab v-model:active-key="activeKey">
    <z-tab-item class="tab-item-doc" key="1" title="用户管理">用户管理</z-tab-item>
    <z-tab-item class="tab-item-doc" key="2" title="配置管理">配置管理</z-tab-item>
    <z-tab-item class="tab-item-doc" key="3" title="角色管理">角色管理</z-tab-item>
  </z-tab>
</template>
<script>

export default {
  components: {},
  data() {
    return {
      activeKey:"1"
    }
  }
};
</script>
<style lang="scss">
.tab-item-doc {
  padding: 20px 12px;
}
</style>
