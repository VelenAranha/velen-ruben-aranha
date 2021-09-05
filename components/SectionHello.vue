<template>
  <section
    class="
      section-hello
      container
      mx-auto
      flex
      md:flex-row
      flex-col flex-col-reverse
      p-8
    "
  >
    <div class="w-full flex flex-row items-center">
      <div
        class="
          bg-black
          text-white
          flex flex-col-reverse
          items-center
          md:flex-row
          flex-1
        "
      >
        <div class="hello-content-wrap m-8">
          <h1 class="title text-6xl">
            Hello! <br />I'm Velen <br />
            Ruben Aranha
          </h1>
          <p
            class="my-4 uppercase text-3xl bg-white text-black p-2 inline-block"
          >
            Frontend Developer
          </p>

          <div class="download-cv my-8">
            <a class="download-btn" href="" target="_blank" rel="nofollow"
              ><span>DOWNLOAD CV</span></a
            >
          </div>
        </div>
        <div class="flex-1 hello-image-wrap">
          <div class="hello-image">
            <img
              width="440"
              height="718"
              src="@/static/velen.jpeg"
              class="attachment-full size-full"
              alt=""
              loading="lazy"
              sizes="(max-width: 440px) 100vw, 440px"
            />
            <!-- srcset="
          https://demo.cocobasic.com/romea-wp/demo-1/wp-content/uploads/2020/09/profile_image.jpg         440w,
          https://demo.cocobasic.com/romea-wp/demo-1/wp-content/uploads/2020/09/profile_image-184x300.jpg 184w
        " -->
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped lang="scss">
.section-hello {
  height: 800px;
  background-image: url(@/static/modern-art-lines.webp);
  background-position: bottom left;
  background-repeat: no-repeat;
  background-size: cover;
  .hello-content-wrap {
    .title {
      letter-spacing: -2.5px;
    }
    .download-btn {
      color: #fff;
      font-size: 12px;
      position: relative;
      font-weight: 600;
      letter-spacing: 5px;
      &:before {
        content: '';
        width: 30px;
        height: 30px;
        border: 2px solid #fff;
        background: 0 0;
        border-radius: 90%;
        top: -8px;
        position: absolute;
        transition: 0.3s;
      }
      span {
        transition: 0.3s;
        display: inline-block;
        margin-left: 50px;
      }
      &:hover {
        span {
          transform: translateX(-8px);
        }
        &:before {
          width: calc(100% + 30px);
          height: 52px;
          border-radius: 50px;
          top: -18px;
        }
      }
    }
  }
  .hello-image-wrap {
    position: relative;
    @apply flex flex-row items-center content-center;
  }
  .hello-image {
    width: 250px;
    height: 250px;
    border: 1px solid black;
    border-radius: 50%;
    overflow: hidden;
    @screen lg {
      position: absolute;
      left: 50%;
      top: 50%;
      width: 440px;
      height: auto;
      transform: translate(-50%, -50%);
      border: 24px double black;
      border-radius: 4px;
    }
  }
}
</style>
