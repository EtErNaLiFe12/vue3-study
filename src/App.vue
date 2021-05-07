<!-- <template>
  <Fruits />
</template>

<script>
import Fruits from '~/components/Fruits'
export default {
  components: {
    Fruits
  }
}
</script> -->

<!-- -------------computed(계산된 데이터) 캐싱 / Getter / Setter--------------------------- -->

<!--
<template>
  <button @click="add">
    ADD
  </button>  
  <h1>{{ msg.split('').reverse().join('') }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      // GETTER(값을 얻어내는 용도), SETTER (값을 지정하는 용도)
      msg: 'Hello Computed!'
    }
  },
  computed: {
    // GETTER - 값을 얻어내는 용도
    // reversedMessage() {
    //   return this.msg.split('').reverse().join('')
    // }
    // Getter, Setter
    reversedMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(newValue) {
        this.msg = newValue
      }
    }
  },
  // methods: {
  //   reverseMessage() {
  //     return this.msg.split('').reverse().join('')
  //   }
  // }
  methods: {
    add() {
      this.reversedMessage += '!?'
      // this.msg += '!?'
    }
  }
}
</script>
-->

<!-- -----------------watch--------------------- -->
 
<template>
  <h1 @click="changeMessage"> 
    <!-- v-on:click => @click -->
    {{ msg }}
  </h1>
  <h1>{{ reversedMessage }}</h1>
  <!-- <h1>{{ changeMessage() }}</h1> -->
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello?'
    }
  },
  computed: {
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  watch: { // 변경을 감시하는 부분
    msg(nv) { // method () 괄호 안에 명칭을 추가해도 됨 (원하는 이름으로 설정 가능)
      console.log('msg:', nv)
    },
    reversedMessage() {
      console.log('reversedMessage:', this.reversedMessage)
    }
  },
  methods: {
    changeMessage() {
      this.msg = 'Good!'
    }
  }
}
</script>

<!-- ---------------------------------------------- -->