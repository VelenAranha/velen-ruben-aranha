<template>
  <div class="page">
    <section-hello />
    <section-about />
    <section-skills />
    <section-work />
    <section class="section-blog container mx-auto flex-col p-8">
      <h2 class="text-4xl text-black mb-8">Blogs</h2>
      <div>
        <script async src="https://static.medium.com/embed.js"></script>
        <a
          class="m-story"
          href="https://medium.com/@velenra/using-angular-material-spinner-with-cdk-overlay-8ab92bfbafee"
          >Using Angular material spinner with cdk overlay</a
        >
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import SectionHello from '@/components/SectionHello.vue'
import SectionSkills from '@/components/SectionSkills.vue'
import SectionAbout from '@/components/SectionAbout.vue'
import SectionWork from '@/components/SectionWork.vue'
import Vue from 'vue'

export default Vue.extend({
  components: { SectionHello, SectionSkills, SectionAbout, SectionWork },
})
</script>
