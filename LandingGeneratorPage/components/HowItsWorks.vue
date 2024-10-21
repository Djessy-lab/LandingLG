<template>
  <div class="sm:w-[100%] lg:w-[60%] mx-auto rounded-3xl shadow-2xl">
    <video autoplay loop muted class="rounded-3xl" :playbackRate="5">
      <source src="/public/img/video.mov" type="video/mp4">
    </video>
  </div>
</template>


<script>
export default {
  name: 'HowItsWorks',
  props: {
    imgArg: { type: String, default: "" },
  }
}
</script>
