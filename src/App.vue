<!-- <template>
  <button @click="handler">
    Click me!!
  </button>
  <ul>
    <li
      v-for="{id, name} in newFruits"
      :key="id">
      // 각각의 데이터가 고유한지를 확인하기 위해 키값으로 고유한 값을 설정함.
      {{ name }}-{{ id }}
    </li>
  </ul>
</template>

<script>
import shortid from 'shortid'
export default {
  data() {
    return {
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  computed: {
    newFruits() {
      return this.fruits.map(fruit => ({
        id: shortid.generate(), // 고유한 값들이 필요할때 shortid 패키지 사용
        name: fruit
      }))
    }
  },
  methods: {
    handler() {
      this.fruits.push('Orange') // 배열데이터 뒷쪽으로 새로운 데이터를 밀어 넣을 수 있다.
    }
  }
}
</script> -->

<!-- ---------------------------------------------- -->
<!-- 이벤트 핸들링 -->

<!-- <template>
  <button @click="handler('hi', $event)"> // $event - 이벤트 객체 표시
    Click 1
  </button>
  <button @click="handler('what', $event)">
    Click 2
  </button>
</template>

<script>
export default {
  methods: {
    handler(msg, event) {
      // console.log(event)
      // console.log(event.target.textContent)
      console.log(msg)
      console.log(event)
    }
  }
}
</script> -->

<!-- ---------------------------------------------- -->

<!-- <template>
  <button @click="handlerA(), handlerB()">
    Click me!
  </button>
</template>

<script>
export default {
  methods: {
    handlerA() {
      console.log('A')
    },
    handlerB() {
      console.log('B')
    }
  }
}
</script> -->

<!-- ---------------------------------------------- -->

<!-- <template>
  <a 
    href="https://naver.com"
    target="_blank"
    @click.prevent.once="handler"> 
    NAVER
  </a>
</template>

<script>
export default {
  methods: {
    // handler(event) {
    //   event.preventDefault() // 기본동작을 방지하고 메소드만 출력할때
    //   console.log('ABC')
      handler() {
        console.log('ABC!')
      }
    }
  }
</script> -->

<!-- ---------------------------------------------- -->

<!-- <template>
  <div
    class="parent"
    @click.capture="handlerA">
    <div
      class="child"
      @click.stop="handlerB"></div>
  </div>
</template>

<script>
export default {
  methods: {
    handlerA() {
      console.log('A')
    },
    handlerB() {
      // event.stopPropagation() // 이벤트 버블링 방지 (b만 출력되게함)
      console.log('B')
    }
  }
}
</script>

<style scoped lang="scss">
  .parent {
    width: 200px;
    height: 100px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    .child {
      width: 100px;
      height: 100px;
      background-color: orange;
    }
  }
</style> -->

<!-- ---------------------------------------------- -->

<!-- <template>
  <div
    class="parent"
    @click.self="handlerA">
    <div
      class="child"></div>
  </div>
</template>

<script>
export default {
  methods: {
    handlerA(event) {
      console.log(event.target)
      console.log(event.currentTarget)
      console.log('A')
    },
    handlerB() {
      // event.stopPropagation() // 이벤트 버블링 방지 (b만 출력되게함)
      console.log('B')
    }
  }
}
</script>

<style scoped lang="scss">
  .parent {
    width: 200px;
    height: 100px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    .child {
      width: 100px;
      height: 100px;
      background-color: orange;
    }
  }
</style> -->

<!-- ---------------------------------------------- -->

<!-- <template>
  <div
    class="parent"
    @wheel.passive="handler"> // passive를 통해 처리 로직과 화면 스크롤을 독립시켜줌 - 부하를 줄이고 부드럽게 스크롤이 되며 내부적으로 로직 처리됨.(속도는 최대 5배 이상 빨라짐)
    <div
      class="child"></div>
  </div>
</template>

<script>
export default {
  methods: {
    handler(event) {
      for (let i = 0; i < 10000; i += 1)
      console.log(event) // 이벤트 객체를 출력
    }
  }
}
</script>

<style scoped lang="scss">
  .parent {
    width: 200px;
    height: 100px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    overflow: auto;
    .child {
      width: 100px;
      height: 2000px;
      background-color: orange;
    }
  }
</style> -->

<!-- ---------------------------------------------- -->

<template>
  <input
    type="text"
    @keydown.ctrl.shift.a="handler" />
</template>

<script>
export default {
  methods: {
    handler(event) {
      // if(event.key === 'Enter') {
        console.log('Enter!!')
      // }
      console.log(event)
    }
  }
}
</script>