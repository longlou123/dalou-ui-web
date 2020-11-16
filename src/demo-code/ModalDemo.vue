<demo>示例代码</demo>
<template>
  <z-modal :top="styles" :width="widths" :visibles="modalV" @changeModel="changeModel">
    <template v-slot:title>
      <span class="modal-title-doc">标题</span>
    </template>
    <template v-slot:content>
      <div class="content-doc">展示的内容</div>
    </template>
  </z-modal>
</template>
<script>
export default {
  data() {
    return {
      modalV: false,
      styles: '100px',
      widths: "60%"
    }
  },
  components: {},
  methods: {
    changeModel(val) {
      console.log(val)
      if(val === "ok"){
        this.modalV = false
      }else if(val === "cancel"){
        this.modalV = false
      }else{
        this.modalV = false
        console.log('关闭')
      }
    }
  }
}
</script>
