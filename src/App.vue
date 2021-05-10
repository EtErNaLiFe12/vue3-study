<!-- CLASS BINDING -->
<!-- <template>
  <h1
    :class="{ active: isActive }"
    @click="activate">
    Hello?!({{ isActive }})
  </h1>
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    activate() {
      this.isActive = true
    }
  }
}
</script>

<style scoped>
  .active {
    color: red;
    font-weight: bold;
  }
</style> -->

<!-- ---------------------------------------- -->
<!-- STYLE BINDING -->

<!-- <template>
  <h1
    :style="{
      color, // 객체 데이터에서 속성의 이름과 데이터의 이름이 동일시에는 color하나만 적어줄수 있음 color: color, => color,
      fontSize
    }"
    @click="changeStyle">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      color: 'orange',
      fontSize: '30px'
    }
  },
  methods: {
    changeStyle() {
      this.color = 'red'
      this.fontSize = '50px'
    }
  }
}
</script> -->

<!-- ---------------------------------------- -->
<!-- 배열구문 -->
<!-- <template>
  <h1
    :style="[ fontStyle, backgroundStyle ]"
    @click="changeStyle">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      fontStyle: {
        color: 'orange',
        fontSize: '30px'
      },
      backgroundStyle: {
        backgroundColor: 'black'
      }
    }
  },
  methods: {
    changeStyle() {
      this.fontStyle.color = 'red'
      this.fontStyle.fontSize = '50px'
    }
  }
}
</script> -->
<!-- ---------------------------------------- -->
<!-- 조건부 렌더링 v-if / else -->
<!-- <template>
  <button @click="handler">
    Click me!
  </button>
  <h1 v-if="isShow">
    Hello?!
  </h1>
  <h1 v-else-if="count > 3">
    Count > 3
  </h1>
  <h1 v-else>
    Good~
  </h1>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
      count: 0
    }
  },
  methods: {
    handler() {
      this.isShow = !this.isShow
      this.count += 1
    }
  }
}
</script> -->

<!-- ---------------------------------------- -->
 <!-- <template>
  <button @click="handler">
    Click me!
  </button>
   // <div v-if="isShow">
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p> 
  // </div> 
  <template v-if="isShow">
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </template>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
      count: 0
    }
  },
  methods: {
    handler() {
      this.isShow = !this.isShow
      this.count += 1
    }
  }
}
</script> -->

<!------------------ v-show-------------------- -->

<template>
  <button @click="handler">
    Click me!
  </button>
  <h1 v-show="isShow">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      isShow: false,
      count: 0
    }
  },
  methods: {
    handler() {
      this.isShow = !this.isShow
      this.count += 1
    }
  }
}
</script>

