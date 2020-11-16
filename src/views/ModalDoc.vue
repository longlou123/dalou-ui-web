<template>
  <demo-doc title="基本用法" description="弹出一个对话框" :component="ModalDemo" :modal="Modal_M"></demo-doc>
  <!-- <demo-doc title="函数式调用" description="隐藏dom结构，只暴露出调用的api" :component="ModalDemo1"></demo-doc> -->
  <attr :columns="columns" :data="data"></attr>
</template>
<script>
import DemoDoc from '../components/Demo.vue';
import ModalDemo from '../demo-code/ModalDemo.vue';
import Modal_M from '../demo-code/Modal_M.vue';
import ModalDemo1 from '../demo-code/ModalDemo1.vue';
import {columns} from '../lib/data';
import Attr from '../components/Attr.vue';

export default {
  components: {Attr, DemoDoc},
  setup() {
    const data = [
      {
        params: 'visible',
        desc: '是否展示',
        type: 'boolean',
        select: 'true / false',
        default: 'normal',
      },
      {
        params: 'changeModel',
        desc: '关闭/取消/确认回调函数',
        type: 'function',
        select: 'ok/cancel/close',
        default: '--',
      },
      // {
      //   params: 'cancel',
      //   desc: '取消触发函数',
      //   type: 'function',
      //   select: '()=>{}',
      //   default: '--',
      // },
    ];
    return {
      ModalDemo,
      Modal_M,
      ModalDemo1,
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
