<template>
  <div>
    <h1>{{ animal.name }} is a {{ $route.params.species }}</h1>
    <p>{{ animal.age }} Years Old</p>
    <p>Breed is {{ animal.breed }}</p>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  data () {
    return {
      animal: {}
    }
  },
  computed: {
    ...mapState(['cats', 'dogs'])
  },
  mounted () {
    // this.cats
    // this['cats']
    const animals = this[this.$route.params.species][this.$route.params.id]
    this.animal = animals
  }
}
</script>
