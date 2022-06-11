<template>
  <div class="slider" style="background: url('/insta1.png') no-repeat">
    <div class="slider-image">
      <client-only placeholder="Loading...">
        <agile
          :dots="false"
          :autoplay="true"
          :autoplay-speed="5000"
          :fade="true"
          :change-delay="400"
          :speed="2500"
          :nav-buttons="false"
        >
          <div class="slide">
            <img src="/1.jpg" />
          </div>
          <div class="slide">
            <img src="/2.jpg" />
          </div>
          <div class="slide">
            <img src="/3.jpg" />
          </div>
        </agile>
      </client-only>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.slider {
  @apply h-full relative;
}
.slider-image {
  @apply relative;
}
</style>
