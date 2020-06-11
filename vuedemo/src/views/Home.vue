<template>
  <div class="home">{{count}}</div>
</template>

<script>
// @ is an alias to /src
import { mapState } from 'vuex'

export default {
  name: 'Home',
  computed: {
    ...mapState(['count'])
  },
  methods: {
    increment () {
      this.$store.commit('increment')
      console.log(this.$store.state.count)
    }
  }
}
</script>
