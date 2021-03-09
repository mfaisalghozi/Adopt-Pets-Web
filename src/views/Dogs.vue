<template>
  <div>
    <h1>Dogs For Sale</h1>
    <b-table striped hover :items="dogs">
      <template #cell(name)="data">
        <a :href="`/pet/dogs/${data.index}`">{{ data.value }}</a>
      </template>
    </b-table>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  data () {
    return {}
  },
  computed: {
    ...mapState([
      'dogs'
    ])
  }
}
</script>
