<template>
  <button class="my-button" @click.end="clickFunc">
    <!-- slotはコンポーネントの間に入れたDOMが入るところ -->
    <!-- <my-button>おしてね</my-button> -->
    <!-- 上の例だとボタンの中におしてねが書かれた状態でレンダリングされます -->
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'MyButton',
  methods: {
    clickFunc (e) {
      this.$emit('click', e)
    }
  }
}
</script>

<style scoped>
.my-button {
  border: none;
  padding: 8px 32px 8px 32px;
  border-radius: 8px;
  background-color: #66BB6A;
  font-size: 100%;
  width: 256px;
  height: 32px;
}
.my-button:hover {
  background-color: #388E3C
}
.my-button:active {
  background-color: #757575
}
</style>
