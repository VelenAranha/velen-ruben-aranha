<template>
  <section
    class="
      section-skills
      container
      mx-auto
      flex flex-col
      p-8
      bg-white
      text-black
    "
  >
    <h2 class="text-4xl mb-8">About Work</h2>
    <div class="flex flex-col">
      <div class="description flex-1">
        <p class="my-4">
          I started my career at Pacewisdom Solutions, a startup experience,
          that laid a strong foundation for my professional career. I have
          worked on a few projects which fall under different domains such as
          finance, field force management, real estate, and blog apps. In my
          current company, Robosoft Technologies, I’m working on a project which
          is a digital wallet domain hybrid application and has a huge user base
          in Japan.
        </p>
      </div>
      <div class="work-experiences flex md:flex-row flex-col mr-8">
        <div class="experience flex-1 my-2">
          <p class="font-bold uppercase">feb 2019 - present</p>
          <p>
            Robosoft Technologies<br /><a
              class="web-link"
              href="https://www.robosoftin.com/"
              >https://www.robosoftin.com/</a
            >
          </p>
        </div>
        <div class="experience flex-1 my-2">
          <p class="font-bold uppercase">aug 2017 - feb 2019</p>
          <p>
            Pacewisdom solutions<br /><a
              class="web-link"
              href="https://pacewisdom.com/"
              >https://pacewisdom.com/</a
            >
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.web-link {
  @apply font-bold;
  position: relative;
  z-index: 0;
  transition: color 0.3s;
  &::after {
    content: '';
    display: block;
    width: 102%;
    height: 6px;
    background-color: #96dfff;
    position: absolute;
    transition: bottom 0.3s;
    left: -1%;
    bottom: 1px;
    z-index: -1;
  }
  &:hover {
    &::after {
      bottom: -10px;
    }
  }
}
</style>
