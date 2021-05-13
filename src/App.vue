<!--단방향 데이터 바인딩

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text" 
    :value="msg" />
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!'
    }
  }
}
</script> -->


<!--양방향 데이터 바인딩 1

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text" 
    :value="msg" 
    @input="handler" />
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!'
    }
  },
  methods: {
    handler(event) {
      console.log(event.target.value)
      this.msg = event.target.value
    }
  }
}
</script>-->


<!--양방향 데이터 바인딩 2

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text" 
    :value="msg" 
    @input="msg = $event.target.value" />
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!'
    }
  }
}
</script>-->


<!--양방향 데이터 바인딩 3
<template>
  <h1>{{ msg }}</h1>
  <input
    type="text"
    :value="msg"
    @input="msg = $event.target.value" />
  <h1>{{ checked }}</h1>
  <input
    type="checkbox"
    v-model="checked" />
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!',
      checked: false
    }
  }
}
</script> -->

<!--v-model 수식어-1

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text"
    :value="msg"
    @change="msg = $event.target.value" />
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!'
    }
  }
}
</script>-->

<!--v-model 수식어-1-1

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text"
    v-model.lazy="msg" /> 
</template>

<script>
export default {
  data() {
    return {
      msg: 123
    }
  },
  watch: {
    msg() {
      console.log(typeof this.msg)
    }
  }
}
</script>-->

<!--v-model 수식어-2

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text"
    v-model.number="msg" /> 
</template>

<script>
export default {
  data() {
    return {
      msg: 123
    }
  },
  watch: {
    msg() {
      console.log(typeof this.msg)
    }
  }
}
</script>-->

<!--v-model 수식어-3-->

<template>
  <h1>{{ msg }}</h1>
  <input
    type="text"
    v-model.trim="msg" /> 
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!'
    }
  },
  watch: {
    msg() {
      // console.log(this.msg.trim())
      console.log(this.msg)
    }
  }
}
</script>

