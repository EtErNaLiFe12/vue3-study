<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 2
    }
  },
  beforeCreate() {
    console.log('Before Create!', this.count)
  },
  created() { // lifecycle hook 컴포넌트 생성 직후
    console.log('Created!', this.count)
    console.log(document.querySelector('h1'))
  },
  beforeMount() { // 컴포넌트 연결 전
    console.log('Before Mount!')
    console.log(document.querySelector('h1'))
  },
  mounted() { // 컴포넌트 연결 직후
    console.log('Mounted!')
    console.log(document.querySelector('h1'))
  }
}
</script>

