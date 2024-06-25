<template>
  <div class="col-10 col-sm-7 col-lg-7 mx-auto hero-image-container">
    <img
      :alt="alt"
      class="d-block mx-lg-auto img-fluid hero-image"
      loading="lazy"
      :src="require(`@/assets/images/${src}`)"
    />
  </div>
</template>
<script>
export default {
  props: ["src", "alt"],
};
</script>
<style>
img {
  max-width: 100%;
  height: auto;
}

@media (max-width: 576px) {
  .hero-image {
    margin-top: 100vh;
  }
}

@media (min-width: 577px) and (max-width: 768px) {
  .hero-image {
    margin-top: 30vh;
  }
}
</style>
