<template>
  <Market />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Market from './components/Market.vue'

export default defineComponent({
  name: 'App',
  components: {
    Market
  }
})
</script>