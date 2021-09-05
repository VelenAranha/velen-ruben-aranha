<template>
  <span class="skill"> {{ skill }} </span>
</template>

<script lang="ts">
import { computed, defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  props: {
    skill: { type: String, required: true },
  },
})
</script>

<style lang="scss" scoped>
.skill {
  border-radius: 50px;
  @apply inline-block bg-white text-black uppercase text-xs p-4 font-bold mx-1 my-2;
  letter-spacing: 5px;
}
</style>
