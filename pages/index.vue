<template>
  <div class="cont">
    <div class="md:block hidden">
      <SliderImage />
    </div>
    <div>
      <InstaLoginForm />
    </div>
  </div>
</template>

<script>
import SliderImage from '../components/sliderImage.vue'
import InstaLoginForm from '../components/InstaLoginForm.vue'

export default {
  name: 'IndexPage',
  components: { SliderImage, InstaLoginForm },
}
</script>
<style>
.cont {
  @apply h-screen pt-8 grid md:grid-cols-2 gap-8 max-w-4xl md:m-auto mx-2;
}
</style>
