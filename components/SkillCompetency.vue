<template>
  <div class="skill-competency">
    <div class="skill">
      <div class="skill-text uppercase">{{ skillName }}</div>
      <div class="skill-fill" :style="{ width: ratingPercent }"></div>
      <div class="skill-fill-mask" :style="{ width: maskPercent }"></div>
    </div>
    <div class="skill-num">{{ ratingPercent }}</div>
  </div>
</template>

<script lang="ts">
import { computed, defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  props: {
    rating: { type: Number, required: true },
    skillName: { type: String, required: true },
  },
  setup({ rating }) {
    console.log('props')

    const ratingPercent = computed(() => rating + '%')
    const maskPercent = computed(() => rating + 2 + '%')
    return {
      ratingPercent,
      maskPercent,
    }
  },
})
</script>

<style lang="scss" scoped>
.skill {
  &-competency {
    display: flex;
    align-items: center;
    margin-bottom: 30px;
    justify-items: center;
    height: 60px;
    position: relative;
  }

  &-competency:after {
    clear: both;
    display: block;
    content: '';
  }

  &-percent {
    font-size: 45px;
    line-height: 100%;
    font-weight: 700;
    width: 100px;
    float: right;
    color: #554247;
    letter-spacing: -1px;
  }

  & {
    width: calc(100% - 70px);
    height: 3px;
    background-color: #545454;
    position: relative;
  }

  &-text {
    color: #000;
    font-size: 12px;
    line-height: 100%;
    font-weight: 600;
    letter-spacing: 5px;
    position: relative;
    z-index: 3;
    transform: translateY(-50%);
    top: 50%;
    left: 35px;
    vertical-align: top;
    display: inline-block;
  }

  &-fill {
    position: absolute;
    top: -30px;
    left: 0;
    width: 10%;
    height: 60px;
    transition: width 0.7s;
    background-color: #fff;
    max-width: 97%;
    z-index: 2;
  }

  &-fill-mask {
    width: 10%;
    position: absolute;
    top: -30px;
    left: 0;
    height: 60px;
    transition: width 0.7s;
    background-color: #000;
    z-index: 1;
    max-width: 99%;
  }

  &-num {
    font-size: 22px;
    color: #fff;
    margin-left: 30px;
  }
}
</style>
