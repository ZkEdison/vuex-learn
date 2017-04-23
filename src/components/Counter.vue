<template lang="html">
  <div class="">
    Clicked: {{$store.state.count}} times, count is {{evenOrodd}}
    <hr>
    <button type="button" @click="increment">+</button>
    <button type="button" @click="decrement">-</button>
    <br>
    <button type="button" @click="incrementIfOdd">Increment if odd</button>
    <br>
    <button type="button" @click="incrementAsync">Increment async</button>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
  computed: mapGetters([
    'evenOrodd'
  ]),
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
  ])
}
</script>

<style lang="css">
</style>
