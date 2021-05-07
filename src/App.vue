<template>
  <!-- <h1 
    v-once
    @click="add">
    {{ msg }}
  </h1>
  <h1 v-html="msg"></h1> -->
  <h1
    :[attr]="'active'"
    @[event]="add">
    <!--v-bind: 으로 데이터를 삽입 가능  -->
    {{ msg }}
  </h1>
</template>

<script>
export default {
  data() {
    return {
      // msg: '<div style="color: red;">Hello!!</div>'
      msg: 'active',
      attr: 'class',
      event: 'click'
    }
  },
  methods: {
    add() {
      this.msg += '!'
    }
  }
}
</script>

<style scoped>

.active {
  color: royalblue;
  font-size: 100px;
}
</style>