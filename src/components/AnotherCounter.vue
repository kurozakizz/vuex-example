<template>
  <div>
    <button class="btn btn-primary" @click="asyncIncrement({ by: 50, duration: 500 })">Async Increment</button>
    <button class="btn btn-primary" @click="asyncDecrement({ by: 50, duration: 500 })">Async Decrement</button>
  </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  methods: {
    ...mapActions([
      'asyncIncrement',
      'asyncDecrement'
    ])

    // ...mapMutations([
    //   'increment',
    //   'decrement'
    // ]),

    // increment() {
    //   this.$store.commit('increment')
    // },
    // decrement() {
    //   this.$store.commit('decrement')
    // }
  }
};
</script>