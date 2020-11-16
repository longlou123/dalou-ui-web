<template>
  <div class="container">
    <demo-doc title="tab切换" description="内容有关联的不同类型的数据" :component="TabDemo" :modal="TabModal"></demo-doc>
    <attr :columns="columns" :data="data"></attr>
  </div>
</template>

<script>
import DemoDoc from '../components/Demo.vue';
import TabDemo from '../demo-code/TabDemo.vue';
import TabModal from '../demo-code/TabModal.vue';
import {columns} from '../lib/data.ts';
import Attr from '../components/Attr.vue';

export default {
  components: {Attr, DemoDoc},
  setup() {
    const data = [
      {
        params: 'key',
        desc: '绑定值，选中选项卡的 name',
        type: 'string',
        select: '--',
        default: '第一个选项卡的 name',
      },
      {
        params: 'title',
        desc: '选项卡标题',
        type: 'string',
        select: '--',
        default: '--',
      },

    ];

    return {
      TabDemo,
      TabModal,
      columns,
      data,
    };
  },
};
</script>

<style lang="scss" scoped>
.show-content {
  padding: 40px 20px;
}
</style>
