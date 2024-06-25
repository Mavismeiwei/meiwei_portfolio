<template>
  <section
    class="vh-100 d-flex justify-content-center align-items-center hero-section"
  >
    <div class="container py-5">
      <div class="row flex-lg-row-reverse align-items-center g-md-5 py-5">
        <slot name="picture"></slot>
        <slot></slot>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "HeroContainer",
  props: ["delay"],
};
</script>
<style scoped>
@media (max-width: 576px) {
  .vh-100 {
    height: auto;
    min-height: 100vh;
  }
}

@media (min-width: 577px) and (max-width: 768px) {
  .vh-100 {
    height: auto;
    min-height: 50vh;
  }
}
</style>
