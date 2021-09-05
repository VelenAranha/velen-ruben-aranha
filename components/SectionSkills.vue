<template>
  <section class="section-skills container mx-auto flex flex-col p-8 bg-black">
    <h2 class="text-4xl text-white mb-8">Tech that I work on</h2>
    <div>
      <skill v-for="skill of skills" :key="skill" :skill="skill" />
    </div>
  </section>
</template>

<script lang="ts">
import Skill from '@/components/Skill.vue'
import { defineComponent } from '@nuxtjs/composition-api'
export default defineComponent({
  components: { Skill },
  setup() {
    const skills = [
      'vue',
      'angular',
      'react',
      'typescript',
      'scss',
      'javascript',
      'html',
      'css',
      'jest',
      'node',
      'git',
      'rest Api',
      'Jira',
      'Confluence',
    ]
    return { skills }
  },
})
</script>

<style scoped lang="scss"></style>
