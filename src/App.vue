<template>
  <!-- <h1 
    v-once
    @click="add">
    {{ msg }}
  </h1>
  <h1 v-html="msg"></h1> -->

  <!--v-bind: 으로 데이터를 삽입 가능  -->
  <h1
    :[attr]="'active'" 
    @[event]="add">
    <!-- v-bind:class => :class or :[동적전달인자] 사용 가능  -->
    <!-- v-on:click => @click or @[동적전달인자] 사용 가능 -->
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