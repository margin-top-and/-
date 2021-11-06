<template>
  <div>{{num}}</div>
</template>
<script>
import { EventBus } from '../event-bus.js'
export default {
  data () {
    return {
      num: 0
    }
  },
  methods: {
    add () {
      EventBus.$emit('addition', {
        num: this.num++
      })
    }
  }
}
</script>
