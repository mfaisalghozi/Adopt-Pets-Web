<template>
  <div>
    <b-table striped hover :items="cats" />
  </div>
</template>

<script>
import cats from '@/data/cats.js'
export default {
  data () {
    return {
      cats
    }
  }
}
</script>
